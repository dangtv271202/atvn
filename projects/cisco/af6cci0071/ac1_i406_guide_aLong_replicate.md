# Arrive Technologies

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)
<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Arrive Technologies](#arrive-technologies)
- [Model testing](#model-testing)
	- [DUT](#dut)
	- [ATT Eth](#att-eth)
- [Run script](#run-script)

<!-- /TOC -->
# Model testing

ATT ETH <-> ARAD <-> DUT, loop-back Sonet

## DUT

- telnet 172.33.42.40
- user:root
- cd /media/ram/quangnm/sdk_debug
- ./epapp -n
- cisco slot add 3

## ATT Eth

- telnet 172.33.42.40
- user: root
- cd /media/ram/quangnm/3G_ATT
- ./epapp -n
- cisco slot ad 0

# Run script

- Step 1:
```
DUT: Run script : tcl ../debug/imsg_aLong/dut_normal_vc3.tcl
ATT: Run script : tcl ../debug/imsg_aLong/att_normal_vc3.tcl
===> Check all status is OK
```
- Step 2:
```
DUT: Run script unbind_bind: tcl ../debug/imsg_aLong/dut_normal_vc3_unbind_bind.tcl
```
- Step 3: Check all status both DUT & ATT are OK (check affect at the ATT:
```
show att eth flow counters 2-12,14-15,17-27,31-32,34-43,45,47-48,52-56,58-61,63-64,66-69,71-73,77-81,83,85,87-90,92-98,100-102,104-106,108-115,117,119-120,124-125,127-131,133-135,139-144,147-149 ro)
```
- Step 4:
```
DUT: Run script : tcl ../debug/imsg_aLong/dut_normal_vc3_hdlc.tcl
ATT: Run script : tcl ../debug/imsg_aLong/att_normal_vc3_hdlc.tcl
===> Check all status is OK
```
- Step 5:
```
 Run script unbind_bind: tcl ../debug/imsg_aLong/dut_normal_vc3_hdlc_unbind_bind.tcl
```
- Step 6: Check affect at the ATT:
```
show att eth flow counters 6,8,12-15,19,21-25,27-31,34-35,37-38,40-42,44-47,49,52,54,56,58-59,61,64,67,69,71,74,80-82,84-86,88-92,95-96,98,101-102,105-110,114,116,118-121,123,125,127-129,131,134-136,139-142,144,147,150 ro
===> (some changed channels have error pkt)
```
