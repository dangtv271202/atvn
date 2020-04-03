

# Arrive Technologies

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Arrive Technologies](#arrive-technologies)
- [Purpose](#purpose)
- [Release noted](#release-noted)
	- [Common](#common)
	- [3G MS](#3g-ms)
	- [10G MS](#10g-ms)
- [Steps/topology to recreate fixed issues](#stepstopology-to-recreate-fixed-issues)
	- [FPGA](#fpga)
		- [Support: All TOH bytes will be generated from framer when disable TOH PW function](#support-all-toh-bytes-will-be-generated-from-framer-when-disable-toh-pw-function)
		- [Fix issue: Counter payload plus 1-byte per packet in HDLC protocol (Arrive's internal issue)](#fix-issue-counter-payload-plus-1-byte-per-packet-in-hdlc-protocol-arrives-internal-issue)
	- [SDK](#sdk)
		- [Includes lastest fixes of ```CEM hardenning``` version](#includes-lastest-fixes-of-cem-hardenning-version)
		- [Fix issue ACR timing mode cannot work with ```VC4_Nc``` mode](#fix-issue-acr-timing-mode-cannot-work-with-vc4nc-mode)
		- [Fix issue crash software when calling ```AtObjectToString``` with ```AtSemController``` object](#fix-issue-crash-software-when-calling-atobjecttostring-with-atsemcontroller-object)
		- [Update to prevent not to delete ```HDLC/PPP/MLPPP PWs``` when they are added to ```PW APS group```](#update-to-prevent-not-to-delete-hdlcpppmlppp-pws-when-they-are-added-to-pw-aps-group)
		- [Fix issue: TOH PW for ```OC192 line``` not work when adding full TOH bytes (Arrive's internal issue)](#fix-issue-toh-pw-for-oc192-line-not-work-when-adding-full-toh-bytes-arrives-internal-issue)
		- [Update to limit max payload size in bytes of ```TOH PW is 1024``` as hardware limitation and ```default min``` TOH payload size is ```4 frames```](#update-to-limit-max-payload-size-in-bytes-of-toh-pw-is-1024-as-hardware-limitation-and-default-min-toh-payload-size-is-4-frames)
		- [Fix HA issue relates to database of jitter buffer in packets, ```VC4-Nc services```, and resequence of MLPPP](#fix-ha-issue-relates-to-database-of-jitter-buffer-in-packets-vc4-nc-services-and-resequence-of-mlppp)

<!-- /TOC -->

# Purpose

Cisco requested:
On 3/26/2020 7:06 PM, Tamilselvan Srinivasan -X (tasriniv - HCL TECHNOLOGIES LIMITED at Cisco) wrote:
>
> Hi Arrive Team,
>
>  
>
> I see apart from Fast Search other fixes included.
>
> Can you please share the recreate steps for each fix and topology used to validate the fix.
>
> So that we can take care in our testing.
>
>  
>
> Regards,
>
> S.Tamilslevan

# Release noted
Dear Team,

We'd like to release the latest package of 10G MS with following notes

1. FPGA version: 5.0_10.62

2. FPGA release notes
+ Support fast searching engine to fix CESoPSN convergence issue on APS switching
+ Support: All TOH bytes will be generated from framer when disable TOH PW function
+ Fix issue: Counter payload plus 1-byte per packet in HDLC protocol  (Arrive's internal issue)
+ Fix issue: TOH PW for OC192 line not work when adding full TOH bytes (Arrive's internal issue)

3. SDK version: 4.4.10

4. SDK release notes



## Common



* Includes lastest fixes of CEM hardenning version:
    + Fix issue running full 48 STS-1/VC3 iMSG services, but STS-1/VC3 (has hardware ID is 47) is not configured in the last. Then unbind all encap channels (except encap channel of this STS-1/VC3). Then bind them all again, one of encap channels bound to STS-1/VC3 will impact to encap channel of this STS-1/VC3. This issue will impact to iMSG feature of 3G MS and 10G MS products

    + Disable interrupt of concate VC and its sub channels when deleting concate VC to avoid flooding issue on 10G MS

    + Fix HO BERT and EC1 BERT cannot work well on 3G MS

    + Update mode set of Serial line to fix issue changing EC1 mode to DS3/E3 cause failure timeout on 3G MS

* Fix issue ACR timing mode cannot work with VC4_Nc mode
* Fix issue crash software when calling AtObjectToString with AtSemController object
* Update to prevent not to delete HDLC/PPP/MLPPP PWs when they are added to PW APS group
* Update to limit max payload size in bytes of TOH PW is 1024 as hardware limitation and default min TOH payload size is 4 frames
* Fix HA issue relates to database of jitter buffer in packets, VC4-Nc services, and re-sequence of MLPPP



## 3G MS



* Update to fix issue affecting to other channels in iMSG services.



## 10G MS



* Support fast search from FPGA version 5.0 10.01
* Return not applicable if creating PRBS on Faceplate HO VC
* Correct version support XFI discard counter from FPGA version 4.6
* Update to fix issues on MDL/PRM
* Fix issue PW counters are incorrect if running mixing iMSG service with CEM service
* Fix issue cannot get TOH PW interrupt, alarm and counters correctly
* Correct logic disable forward RDI when TIM downstream AIS that raised
* Fix function to force AU4 Rx AIS in case random concatenation


```
ftp://ftp.atvn.com.vn

user: cisco

pwd: bcbjWLTt

folder: ftp://172.33.39.2/Arrive_10G_MS/200315_FPGA_5.0_10.62_SDK_4.4.10/200315_FPGA_5.0_10.62_SDK_4.4.10.ZIP
```

#  Steps/topology to recreate fixed issues
## FPGA
### Support: All TOH bytes will be generated from framer when disable TOH PW function
* Topology: Testset <-> DUT (Device Under Test)
* Sequence:
 - Configure normal traffic. Make sure that traffic is OK
 - Enable TOH PW function: Check TOH bytes can transparent well (value TOH bytes at the Testset have Tx = Rx)
 - Disable TOH PW function, Then check TOH bytes at the Test-set:
  + Expected: Check TOH bytes at the JDSU receive value from framer
  + Previous version: <span style="color:red">It was still received from TOH PW.

### Fix issue: Counter payload plus 1-byte per packet in HDLC protocol (Arrive's internal issue)
* Topology: Testset <-> DUT (Device Under Test)
* Sequence:
  - Configure normal traffic with DCC service. Make sure that traffic is OK
  - At Testset, generated a fixed length = N (Encap solution Packet)
  - At DUT: Check counters at HDLC layer. For Arrive CLI, you can use "show encap hdlc counters dcc.1.line r2c". Check number Byte/1Packet = N' = Total Byte/Total Packet
    + Expected: N=N'
    + Previous version: <span style="color:red">N=N'-1


## SDK
### Includes lastest fixes of ```CEM hardenning``` version
It was covered on the "CEM harderning" version.

### Fix issue ACR timing mode cannot work with ```VC4_Nc``` mode
* Topology: Testset <-> DUT (Device Under Test)
* Sequence:
 - Configure normal data flow with ```oc48/sts-nc``` (Currently, Arrive is supporting n=24). Configure timing ACR or DCR for that path.
  + Expected: Normal traffic must OK, ACR/DCR timing state must change to ```"locked"``` after Sync Clock.
  + Previous version: ACR/DCR timing state can not "locked", state is change continues ```int -> learning -> int -> learning ...```

### Fix issue crash software when calling ```AtObjectToString``` with ```AtSemController``` object

This issue will happen when application enable API log function as soon as calling ```AtDriverCreate()``` API. But API log function is default disable, so this issue will be not seen as usual usage

### Update to prevent not to delete ```HDLC/PPP/MLPPP PWs``` when they are added to ```PW APS group```
When application created HDLC/PPP/MLPP PWs and added them to PW APS group. Then application calls API to delete these HDLC/PPP/MLPPP PWs, SDK will return error and not allow this. This will impact to PW APS group, and to delete PWs, they should be removed out of PW APS group first.

### Fix issue: TOH PW for ```OC192 line``` not work when adding full TOH bytes (Arrive's internal issue)
* Topology: Testset <-> DUT (Device Under Test)
* Sequence:
 - Configure normal traffic with ```OC192```. Make sure that traffic is OK
 - Enable full TOH bytes within STSgroup: ```D1,D10,D11,D12,D2,D3,D4,D5,D6,D7,D8,D9,E1,E2,F1,J0,K1,K2,M1,S1```
 - Check TOH function:
  + Expected: all TOH bytes has working well function.
  + Previous version: <span style="color:red">TOH bytes are receive from frame, not TOH function.

### Update to limit max payload size in bytes of ```TOH PW is 1024``` as hardware limitation and ```default min``` TOH payload size is ```4 frames```
* Topology: Testset <-> DUT (Device Under Test)
* Sequence:
 - Configure normal traffic with OC192. Make sure that traffic is OK
 - Create TOH Pw. Check default Pw payloadsize:
   + Expected: ```4 bytes```
   + Previous version: It's 2 bytes
 - Check max payload size in bytes of TOH PW is ```1024.```
    + Change PW TOH payload is over 1024 (payloadsize = number of TOH bytes * framers). <span style="color:red">Make sure SDK prevents it. It was configured successfully in the previous version.
    + Change payload of TOH PW in range (<1024). Make sure CLI execute OK

### Fix HA issue relates to database of jitter buffer in packets, ```VC4-Nc services```, and resequence of MLPPP

Just correct serializing tool for HA debug. <span style="color:green">It does not affect to service.
