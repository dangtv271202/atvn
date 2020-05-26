
[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)

# How to set-up

We will use python script to measure time between manual and fast CLI. Therefore, you need to Import python lib first login SDK:

```
root@t1040rdb:/media/ram# export PYTHONPATH=/tmp/python/libs/python2.7/:/tmp/python/libs/python2.7/site-packages/:/tmp/python/arrive/AtAppManager/:/tmp/python/arrive/atsdk/:/media/ram/dangtv/Cisco:/tmp/python/arrive/atsdk/:/media/ram/dangtv/Cisco/lib:/tmp/python/arrive/atsdk/:/media/ram/dangtv/Cisco/run
```

## normal With clishell

Telnet board ```172.33.42.40```, add slot 2
```
root@t1040rdb:/media/ram/dangtv/450b000# ./epapp -n -D -l 402
root@t1040rdb:/media/ram/dangtv/450b000# ./clishell -c 402


INFO: Main task ID: 3963
Open file /proc/epapp fail, ignore kernel interrupt
********************************************
*         Arrive Technologies              *
*         Command Line SHELL               *
*             AT SDK                       *
*                                          *
*      WARNING: Authorized Access Only     *
********************************************

<6> Info Init TCL Interpreter DONE
AT SDK >cisco slot add 2
AT SDK >show driver
SDK Built On    : Tue 07 Apr 2020 10:42:51 PM +07
                : dungnt@linuxsws012
Source REV      : On gitcommit=heads/test/product/cisco_autotest-0-geada0f0773612002d490fa132c52d9546d45f7f2
Driver Version  : 4.5.0.b000 (active) (Includes 2.6.26.b003)
Hardware Version:
+------+------------+---------------------------------+----------+
|      |            |                                 |          |
|Device|Product code|Version                          |HAL       |
|      |            |                                 |          |
+------+------------+---------------------------------+----------+
|1(*)  |0x60210071  |5.0 (on 2020/03/28), built: 10.63|0x49c01000|
+------+------------+---------------------------------+----------+
AT SDK >

```

# Fast cli with

Telnet board ```172.33.42.40```, add slot 5

```
root@t1040rdb:/media/ram/dangtv/450b000# ./epapp -n -u tcp:4447
INFO: Main task ID: 3899
Open file /proc/epapp fail, ignore kernel interrupt



********************************************
*         Arrive Technologies              *
*         Command Line SHELL               *
*             AT SDK                       *
*                                          *
*      WARNING: Authorized Access Only     *
********************************************

<6> Info Init TCL Interpreter DONE
AT SDK >cisco slot add 5
AT SDK >show driver
SDK Built On    : Tue 07 Apr 2020 10:42:51 PM +07
                : dungnt@linuxsws012
Source REV      : On gitcommit=heads/test/product/cisco_autotest-0-geada0f0773612002d490fa132c52d9546d45f7f2
Driver Version  : 4.5.0.b000 (active) (Includes 2.6.26.b003)
Hardware Version:
+------+------------+---------------------------------+----------+
|      |            |                                 |          |
|Device|Product code|Version                          |HAL       |
|      |            |                                 |          |
+------+------------+---------------------------------+----------+
|1(*)  |0x60210071  |5.0 (on 2020/03/28), built: 10.63|0x49301000|
+------+------------+---------------------------------+----------+
```

## Run script:

* After log-in the SDK and add slot, run script to measure as below:
```AT SDK >python /media/ram/dangtv/Cisco/run/check_fast_cli.py```
