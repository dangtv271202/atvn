# Linux problems

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)

# Issue

Sometimes, The eclipse is can't run ```debug mode``` after the Linux rebooted.
```
[dangtv@linuxsrv70 ~]$ ping localhost
PING localhost (127.0.0.1) 56(84) bytes of data.

--- localhost ping statistics ---
121 packets transmitted, 0 received, 100% packet loss, time 120000ms
```
===> Can't Ping localhost
```
        RX packets 1991800949  bytes 335431077819 (312.3 GiB)
        RX errors 0  dropped 40002949  overruns 0  frame 0
        TX packets 1592144377  bytes 260468882138 (242.5 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
        device memory 0xf7100000-f717ffff  

eno2: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet6 fe80::9dcc:39bd:171f:1da0  prefixlen 64  scopeid 0x20<link>
        ether 00:25:90:d4:cc:5f  txqueuelen 1000  (Ethernet)
        RX packets 857909345  bytes 147897089444 (137.7 GiB)
        RX errors 0  dropped 31915336  overruns 0  frame 0
        TX packets 876919606  bytes 143590130493 (133.7 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
        device interrupt 20  memory 0xf7200000-f7220000
```  
===> Loss of "lo" interface

# How to fix it

- Ping IT help it with cmd: ```ifup lo```
```
[dangtv@linuxsrv70 ~]$ ping localhost
PING localhost (127.0.0.1) 56(84) bytes of data.
64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.012 ms
64 bytes from localhost (127.0.0.1): icmp_seq=2 ttl=64 time=0.012 ms
```
===> Ping Ok

```
[dangtv@linuxsrv70 ~]$ ifconfig
eno1: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 172.33.34.68  netmask 255.255.224.0  broadcast 172.33.63.255
        inet6 fe80::225:90ff:fed4:cc5e  prefixlen 64  scopeid 0x20<link>
        ether 00:25:90:d4:cc:5e  txqueuelen 1000  (Ethernet)
        RX packets 1991942510  bytes 335441059939 (312.4 GiB)
        RX errors 0  dropped 40007255  overruns 0  frame 0
        TX packets 1592282577  bytes 260523142253 (242.6 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
        device memory 0xf7100000-f717ffff  

eno2: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet6 fe80::9dcc:39bd:171f:1da0  prefixlen 64  scopeid 0x20<link>
        ether 00:25:90:d4:cc:5f  txqueuelen 1000  (Ethernet)
        RX packets 857939525  bytes 147899694099 (137.7 GiB)
        RX errors 0  dropped 31919642  overruns 0  frame 0
        TX packets 876919606  bytes 143590130493 (133.7 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
        device interrupt 20  memory 0xf7200000-f7220000  

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>

```
===> Lo up
