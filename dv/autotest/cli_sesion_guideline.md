
[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)
<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Overview](#overview)
- [Performance](#performance)
- [How to use](#how-to-use)
- [Autotest integration](#autotest-integration)
	- [Network connection model](#network-connection-model)
	- [Quick integration](#quick-integration)
		- [Optimized autotest compatible functions](#optimized-autotest-compatible-functions)
		- [Applying git diff](#applying-git-diff)
		- [SDK version supported](#sdk-version-supported)
		- [MAIN Function](#main-function)

<!-- /TOC -->
# Overview

This library is to work with ATSDK development process. It supports common libraries that can be used for all of projects using ATSDK.

The current version supports:

* [Fast CLI session](atsdk\cli_session). This will work with `epapp` that has CLI server start in TCP mode.


>**NOTE:** The fast CLI session can also work with `epapp` that has CLI server works in UDP mode, but there is a case that some packets are lost, especially the finish packet, this cause broken output sometimes. Beside this, UDP is too slow compare with TCP. To speed up UDP, we may need to do more fine-tuning to find proper configuration for UDP socket.

# Performance

From Auto-test testing, this library help to reduce the mix test-cases from more than 12 hours to 2.5 hours, which is a huge gap. Using this library gives the same performance as running directly on-board. Two key factors that make this much faster than the old way:

* Using TCP instead of UDP. This is for reliable purpose, we will not lost any packets.
* Using CSV instead of XML. This is critical point, XML parsing is too slow with too many CPU load. CSV is much more simple, so it is quick. The internal parsing is also optimized to lazily parse only the requested fields (specified by row and column).

# How to use

This Python library along with related scripts can be installed to be used by any users. To do so,

```bash
git clone http://gitlab.atvn.com.vn/codechip/atsdk_ci.git
cd atsdk_ci
sudo python setup.py sdist bdist_wheel
sudo python -m pip install dist/*.tar.gz
```

And to uninstall it, just

```bash
sudo python -m pip uninstall atsdk_ci
```

Of course, we can also simply run `python setup.py install`, but then we will have trouble when we want to uninstall. So, it would be recommended to use `pip` as above as it manages package properly.

To work with this library without installing it, we need to update the `PYTHONPATH` to have other modules see this library and `PATH` to run scripts of this package. As following sequence.

```bash
git clone http://gitlab.atvn.com.vn/codechip/atsdk_ci.git
export PYTHONPATH=$(pwd)/atsdk_ci:${PYTHONPATH}
export PATH=$(pwd)/atsdk_ci/scripts:${PATH}
```
Or, update package library to IDE (such as Eclipse) to run it.

# Autotest integration

## Network connection model

The current autotest topology is as below:

```
             clis/xml                 shell_port
autotest <--------------> clishell <------------> epapp daemon
(python)    pexpect/      <---------------------------------->
           telnetlib            Target boards (systems)
```

Autotest (implemented by Python) uses `pexpect` or `telnetlib` to login to the target board, then starts `epapp` daemon with CLI shell port, it then also starts a `clishell` to connect to this `epapp` daemon over CLI shell port. All of CLIs from autotest will go through `clishell` to `epapp` and get executed there. XML is returned back to autotest python to parse the CLI output along with CLI result. Typically, CLI result is abstracted by one Python class, let's call it `AtCliResult` class for the below explanation.

There is also one common Python API on autotest that execute CLI and return the result, let's call it `autotest.runCli(cli) -> AtCliResult`

Now with this fast CLI session introduced, we have below topology, actually a new direct connection to the `epapp` daemon implemented by `cli_session`

```
                       cli_session
    +--------------------------------------------------+
    |                                                  |
    |        clis/xml                 shell_port       v '-u tcp:<CLI TCP port>' (epapp option)
autotest <--------------> clishell <------------> epapp daemon
(python)    pexpect/      <---------------------------------->
           telnetlib            Target boards (systems)
```

The `autotest` common library must be updated to make use of this fast CLI session by using this CLI session as default instead of the `telnetlib/pexpect` connection. Below are detail updates:

* Update the way to start `epapp` by giving it the CLI TCP port. This is done by using `-u tcp:<cli_tcp_port>`. UDP will be used if `tcp:` is not specified and we may encounter unexpected result because of packets lost.
* Initiate a `cli_session` instance. See the [Fast CLI session](http://gitlab.atvn.com.vn/codechip/atsdk_ci#fast-cli-session)
* Subclass the `AtCliResult` to wrap CLI result returned by `cli_session` just because interfaces are different (probably namings). Let's call it `CliSessionResult` class. See the class `CliResult` in the [`_cli_session.py`](cli_session/_cli_session.py) for all public attributes and methods (less than 10 public items).
* Update the `autotest.runCli(cli)` to run CLI over `cli_session` and return `CliSessionResult`

>**NOTE :** We still keep the `pexpect/telnetlib` connection to run CLIs that are not fully managed by `cli_session`. The reason is that `cli_session` does not see CLISH layer of the `epapp`, so some additional LAB specific actions such as starting polling tasks or enabling debugging features which are implemented in CLISH layer, will not be executed by `cli_session`. Fortunately, there are not so many CLIs of this kind. And below are CLIs that should be sent over `pexpect/telnetlib` connection (of course, send over `cli_session` works too except additional behaviors mentioned above).
>* `termios tc mode`
>* `aps engine start`
>* `eth port serdes eyescan enable`
>* `sdh line serdes eyescan enable`
>* `sdh line eyescan enable`
>* `eth port eyescan enable`

## Quick integration

### Optimized autotest compatible functions

To easily integrate with `autotest`, this module support the API `cli_session.autotest_result(cli_result)` that takes a `cli_session` result and transform it to autotest result which has all of attributes and methods required by autotest.

And to get values of table in an optimized way, the `Table` object in `AutotestResult` supports below APIs and most of them have similar interfaces in autotest.
* `get_values(self, ids, field_names, is_row_id=True, is_counter_cell=False, is_status_cell=False)`, to be compatible with `ATTestChecker.__getValueFromTable`
* `getCellByRowName(self, row_name, column_id=1)` to be compatible with `ATTableUtil.getCellByRowName`
* `getCellByColumnName(self, column_name, row_id=0)` to be compatible with `ATTableUtil.getCellByColumnName`

### Applying git diff

A recommended implementation has been made by [autotest_integrate.diff](integration/autotest_integrate.diff). Just in case we can to quickly integrate this `cli_session` to any autotest workspace, we can follow these two steps:

* Better to have clean workspace: `git status` can help
* Apply the recommended implementation:
    * `cd <autotest_workspace>`
    * `git apply ${ATSDK_CI}/integration/autotest_integrate.diff -3`

### SDK version supported
* Cisco projects: It's supported from the version `\\172.33.39.6\wdb\users\sw\atsdk\cisco_ms\4.5.0\4.5.0.b000`
BTW, aNam fixed some issues with the latest version now. You can get it here:
```
mkdir cli_session
cd cli_session/
busybox tftp -b 64000 -g -r ../../../users/sw/namnn/cli_session/epapp 172.33.50.106
busybox tftp -b 64000 -g -r ../../../users/sw/namnn/cli_session/clishell 172.33.50.106
chmod +x *
```
* Ciena projects:
- Old version for MRO card, 10G with CAS, PDH, PDH with CAS: It's a local build from aNam. You can get it here: `/home/wdb/users/dv/dangtv/summary/ciena/sdk/autotest_att/`
- New version for 10GMS: Contact a.Chi to build it.

### MAIN Function

We support a new param `cliPortId` in MAIN function to support run cli_session. It will call TCP portId on board. Configure `None` to unuse it.

```python
testModule.connect(ATSystem.SYSTEM_TYPE_ATT, ATSystem.CONNECTION_TELNET, '172.33.42.78', 'root', 'root',
                   '/home/wdb/users/sw/namnn/cli_session_ciena', None,
                   {'productType':ATSystem.PRO_CNC_0021_ATT, 'platform':ATSystem.PLATFORM_CIENA,'portId':'78', 'cliPortId': '9099'})

testModule.connect(ATSystem.SYSTEM_TYPE_DUT, ATSystem.CONNECTION_TELNET, '172.33.42.38', 'root', '',
                 '/media/ram/cli_session', None, {'productType':ATSystem.PRO_CCIO071, 'platform':ATSystem.PLATFORM_CISCO, 'slotId':'5', 'portId':'3805', 'cliPortId': '7077'})
```
