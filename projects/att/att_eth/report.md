# <span style="color:Blue">Arrive Technologies</span>

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)

# 31 Mar, 2020

## version

* FPGA updates:
```
Hi Dang,
I fixed this issue and self-test ok with FPGA & SDK below
FPGA image: \\wdb\wdb\projects\ATT\atteth\6a0e0009_8ge1xge\atteth_6a0e0009_v20_mar_25_2020.rbf
SDK : /home/wdb/projects/ATT/AF6A0E0009/3.4.18.5/b022/epapp -p ep5
Please re-check
https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004917118
```
fpgaload /home/wdb/projects/ATT/atteth/6a0e0009_8ge1xge/atteth_6a0e0009_v20_mar_25_2020.rbf

* SDK: /home/wdb/projects/ATT/AF6A0E0009/3.4.18.5/b022/epapp -p ep5
* show driver:

```
AT SDK >show driver
SDK Built On    : Tue 24 Dec 2019 10:37:53 AM +07
                : vulh@linuxsws003
Source REV      : On gitcommit=heads/product/cisco_att_maintenance-0-g829211eb23c5923b3e434c422768fde1b456b85e-dirty
Driver Version  : 3.4.18.5.b022 (active) (3.4.18.5)
Hardware Version:
+------+------------+---------------------------------+----------+
|      |            |                                 |          |
|Device|Product code|Version                          |HAL       |
|      |            |                                 |          |
+------+------------+---------------------------------+----------+
|1(*)  |0x8a0e0009  |2.0 (on 2020/03/25), built: 20. 4|0x48032000|
+------+------------+---------------------------------+----------+
```

# Check issues

## [ATT_ETH_Tester_8a0e0009: EPort counters can't detect DA type packet (Uni, or multi, or broadcast)][O7-43]

* <span style="color:red">The normal traffic was failed, all Tx Pkt=0

```
AT SDK >show eth flow counter 1-3 r2c
+------+---------+----------+--------+---------+----------+-------+-----------+------------+--------------+------------+
|      |         |          |        |         |          |       |           |            |              |            |
|FlowId|txGoodPkt|txGoodByte|txSpeed |rxGoodPkt|rxGoodByte|rxSpeed|rxSeqErrPkt|rxPrbsErrPkt|rxHeaderErrPkt|rxPortErrPkt|
|      |         |          |        |         |          |       |           |            |              |            |
+------+---------+----------+--------+---------+----------+-------+-----------+------------+--------------+------------+
|1     |0        |0         |10000000|0        |0         |0      |0          |0           |0             |0           |
+------+---------+----------+--------+---------+----------+-------+-----------+------------+--------------+------------+
|2     |0        |0         |1000000 |0        |0         |0      |0          |0           |0             |0           |
+------+---------+----------+--------+---------+----------+-------+-----------+------------+--------------+------------+
|3     |0        |0         |1000000 |0        |0         |0      |0          |0           |0             |0           |
+------+---------+----------+--------+---------+----------+-------+-----------+------------+--------------+------------+
AT SDK >show driver
SDK Built On    : Mon 24 Feb 2020 11:39:08 AM +07
                : minhhv@linuxsrv24.atvn.com.vn
Source REV      : On gitcommit=heads/product/cisco_ms_for_autotest_team_all_AT_TESTER_second_version_3.3.x.x_debug-0-g308b38a7b066e91b347018b71b21c5a6f534cbfd-dirty
Driver Version  : 3.4.18.5.b022 (active) (3.4.18.5)
Hardware Version:
+------+------------+---------------------------------+----------+
|      |            |                                 |          |
|Device|Product code|Version                          |HAL       |
|      |            |                                 |          |
+------+------------+---------------------------------+----------+
|1(*)  |0x8a0e0009  |2.0 (on 2020/03/25), built: 20. 4|0x48032000|
+------+------------+---------------------------------+----------+
AT SDK >
```



# 25 Mar, 2020

## version

### FPGAs

fpgaload /home/wdb/projects/ATT/atteth/6a0e0009_8ge1xge/atteth_6a0e0009_v20_mar_23_2020.rbf

```
+ LUT : 51%
+ RAM: 78%
Backup: \\linuxsrv35\Share4Syn\nguyenht\AF5HTS2011CE24_A5GT_highrst_8ge_1xge _oldmac\Backup\AF5HTS2011CE24_A5GT_mar_23_2020.qar

Update: fix  some issues on  zoho
ATT_ETH_18G:  Mpls novlan 1 label packet format : all error counters raised ( prbserr, seqerr, rxheader err)
-> Fixed -> Ms Hoa re-checked ok so this issue has been not posted on zoho
ATT_ETH_18G: Run full 4096 Flow on port 1G has not well function
https://crmplus.zoho.com/portal/arrivetechnologies#buginfo/403027000002130382/403027000004976054
ATT_ETH_Tester_8a0e0009: EPort counters can't detect DA type packet (Uni, or multi, or broadcast)
https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004917118
ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa
https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004890030```
```
### SDKs
/home/wdb/projects/ATT/atsdk/run/ep5/6A0E0009/autotest/3.4.18.5_b022/epapp -p ep5 -P 6A0E0009

## Status

### SDKs

1. [ATT_ETH_18G: Gen payload PRBS11 but DUT detect all0s][O7-44]
  - 25 Mar: I tried with the latest version but the issue still not fixed. Please help me recheck it.

### FPGAs

1. [ATT_ETH_18G: Run full 4096 Flow on port 1G has not well function][O7-49]
  * <span style="color:green">This issue was fixed</span>
2. [ATT_ETH_Tester_8a0e0009: EPort counters can't detect DA type packet (Uni, or multi, or broadcast)][O7-43]
  * <span style="color:green">Multi/Uni were Ok</span>
  * <span style="color:red">a.Nguyen will update code to fix in case broadcast</span>
3. [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41]
  * <span style="color:red">Loopback but 1G always down.</span> Need to 3GMS team confirm that on DUT. a Nguyen will check with aTri/cHieu.

### New Issues
1. [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53]
  * a Nguyen HT is anayzing it.

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
   [O7-41]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004890030>
   [O7-43]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004917118>
   [O7-44]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004935179>
   [O7-49]: <https://crmplus.zoho.com/portal/arrivetechnologies#buginfo/403027000002130382/403027000004976054>
   [O7-53]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000005402377>
