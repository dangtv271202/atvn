# Arrive Technologies

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)


# Estimate resource

## Trinh Van Dang

* Total workload: ```>100%```
* Full control QA for 10GMS cisco: List Sw items and transfer task for member and check it also. Check the new FPGA with update "interrupt restore", sum status, Support customer, ...
  - Plan: Finish it end of this week. Take about 35% workload.
  - Next release: Update interrupt restore based on the image fix CEM only (Cisco requested): ```6-Apr```.
  - Take about ```65% workload```
* MRO 20G: Full control QA for this project
	- Ticket 101: Support aVC/Onder to debug this issue
	- Ticket 110: Support aDinh/Onder to fix it.
  - Sum status, issue
	- Take about ```30% workload```
* 10GMS Ciena AF6CNC0071: Support c.Hoa's team to confirm some Epass issues. Take about ```5% workload```
* ATT_ETH_18G: Confirm some issues from SW/HW. Take about ```5% worload```

## Nguyen Van Bang

* Total workload: ```To be define.```
* He is helping to research "MACsec" Technologies. Currently he is sharing full workload on this task. BTW, I don't control this task, he is reporting to aMinh directly. Therefore, get his report for more inform task.

## Pham Minh Truong

* Total workload: ```100%```
* Share ```13% woarkload``` to research MACsec
  - Get Bang's report for more inform this task.
* He's mainly working on 10GMS project. He is helping me to QA: interrupt restore, Pm/Fm, interrupt tree, mixing with TOH for next release. Run and analyze the new autotest support ```interrupt restore```
  - Finish QA about 60% test-cases.
  - He's sharing ```90% workload``` to QA this project.

## Nguyen Minh Quang

* Total workload: ```> 100%```
* Share ```2 days``` (full workload) to research MACsec: Take about ```33% worload```
  - Get Bang's report for more inform this task.
* He's mainly working on 10GMS project. He is helping me to QA: Smoke Traffic, Mixing test-cases for next release.  BTW, he's sharing his time to check/debug Imsg service test-case.
  - Finish QA about 80% test-cases for next release.
  - He's sharing ```70% workload``` to QA this project.

## Nguyen Thi Hieu

* Total workload: ```To be define.```
* Because Quang is busy to research MACsec, he will focus 2 days (full workload in this time) for that technologies. Therefore, cHieu will share time to capture his task is this time. Take ```about 33% workload```.
* He will back to a.Tri's team to continues QA after Quang finish ```MACsec task```


# 31 Mar, 2020

## Trinh Van Dang

### Status

* Define mix test-cases for "CEM/Imsg application": added some Kbyte test-cases
	- 30 Mar: ```Finished```. Wait for a.Minh to review it.
  - 31 Mar: Meeting with a Minh and team for this topic (from 3h PM: 4h PM). About my task, I will update:
    + Interrupt flooding: Update interrupt soaking
    + OH over PSN: Update more test-case and detail pass condition.
    + Hope finish it tomorrow.
* 20G MRO:
	- Today I'm mainly working with a Dinh, support him and Onder to check the ticket 110. We just fixed it by a new SDK. Quang will help me to QA the "warm test-case" for this SDK. Hope release to Ciena on tomorrow.
* 10GMS Cisco:
	- As Cisco requested, I collected inform items for the version ```FPGA version 5.0_10.62; SDK version 4.4.10``` and send it to Cisco. aNhan/QC reviewed it today. cTran sent it to Cisco.
	- Sum status from Truong/cHieu
* ATT_ETH_18G: Confirm an issue on zoho with the new FPGA. but, that image was failed, the traffic has not well functional. Wait for Hw to check it.
* ATT_6a210081: Currently the FPGA and SDK are not sync, we must force product code to run it. That is not safe, I'm not sure traffic is Ok after force and any developer join to check it. Therefore, I re-assign it to SW team to update SDK for that case first.

### Plan

* Update "mix test-cases for ```CEM/Imsg application```"
* Help aDinh/Onder debug the ```ticket 110``` on MRO project.
* Full control QA the project ```10GMS Cisco```. We will release to customer a new version 6 Apr.
* Support 10GMS Ciena check Epass issues (If request).
* Confirm some issue on ATT projects (If Hw/SW fix it).

## Pham Minh Truong

### Status

This is his report:

* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore9
    - I'm running and support Mr.Minh to fix some case on automation test
* Re-check model DCC to check old issue
    - AF6CCI0071_DV_DCC: Dump packet is got  2 bytes 0x00 when setup - fcs16 >>> assign for Mr.Nhan
    - AF6CCI0071_DV_DCC: Counter MTU is not working >>> assign for Mr.Khoa
    - AF6CCI0071_DV_DCC: Dump packet at Rx ENCAP is incorrect ( 2 - packets) >>> assign for Mr.Nhan
    - AF6CCI0071_DV_DCC: Eth port count both param rxUndersizePackets and - rxPacketsLen64 >>> rechecked and assign for Mr.Nhan

### Plan

* Continua QA interrupt restore with FPGA AF6CCI0071_10GMS_4.7_10.80_restore9


## Nguyen Minh Quang

### Status

He is focusing full workload to research ```MACsec```. Check that topic to get his task results today.

### Plan

* 20G MRO: Help to scan warm test-case
* 10GMS Cisco: Confirm issue + QA for the next release 6/4

## Nguyen Thi Hieu

### Status

Reconfirm issue, transfer from DV-QuangNm
https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005413188
Activitive: re-check some issue  af6cci0071
   1. AF6CCI0071-CEM-DV: Replace idle code was FAILED in case LOPs
   https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005363281
   --> fixed

   2. AF6CCI0071-CEM-DV: ETH port can not detect Broadcast pkt
   https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005342015
   --> fixed
   But will add other issue:
   "But has other issue add PTCH -> detect DA van sai ==> config Broad but count multi"

   3. AF6CCI0071-DV-Imsg: ETH PORT can not detect OversizePacket
   https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005226033
   --> fixed

   4. AF6CCI0071-DV-Imsg: ETH PORT can not detect OversizePacket
   https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005226033
   --> fixed

   5. AF6CCI0071-DV-Imsg: PW_PPP have TX = 0 in case change MIN packetsize
   https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005214189
   --> re-check new/old fpga 3 time ok So I can't sure it's fixed or not

   6. AF6CCI0071-Mx-DV : PPP: VC3 over BW with cfg = 65,595bytes(92% BW)
   https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005075062
   --> this is issue ATT (added other issue on ATT 3G ETH)
   ATT-ETH-3G-DV: Need SW limit when config over BW
   https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#bugsview/403027000001176047/6

### Plan

* Quang just done task about research ```MACsec```. Therefore, cHieu will back to 3GMS project to QA.

# 30 Mar, 2020

## Trinh Van Dang

### Status

* Define mix test-cases for "CEM/Imsg application": added some Kbyte test-cases
	- 30 Mar: ```Finished```. Wait for a.Minh to review it.
* 20G MRO:
	- Join meeting and debug the ticket 110 issue with a Dinh/Onder.
* 10GMS Cisco:
	- As Cisco requested, I collected inform items for the version ```FPGA version 5.0_10.62; SDK version 4.4.10``` and send it to Cisco. Currently, I'm waiting for aNhan/QC to review it.
	- Sum status from Truong/cHieu
* 10GMS Ciena: Support team to check some ethernet passthrough issues.

### Plan

* Help aDinh/Onder debug the ticket 101 on MRO project.
* Full control QA the project 10GMS Cisco.
* Support 10GMS Ciena check Epass issues (If have free time).
* Confirm issue on ATT_ETH_18G

## Pham Minh Truong

### Status

This is his report:
* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore9
    - I'm trying run new version automation support interrupt restore and analyze result
    - I'm working with Mr.Minh and post result interrupt restore by automation test ASAP

* Setup new model to test old issue (DCC function)
    - I spend time to change model test to re-config for re-check old issue as Mr. Nhan resuquest

### Plan

* Continua QA interrupt restore with FPGA AF6CCI0071_10GMS_4.7_10.80_restore9
* Confirm all issues

## Nguyen Minh Quang

### Status

He is focusing full workload to research ```MACsec```. Check that topic to get his task results today.

### Plan

* Continues research ```MACsec```. He will final task on the tomorrow.

## Nguyen Thi Hieu

### Status

* Run auto and analyze result for 3GMS. aTri will report this case.

```
Time = 1:
7) RAN TEST CASE NUMBER     : 29
8) PASSED TEST CASE NUMBER  : 1    (3.44827586207%)
9) FAILED TEST CASE NUMBER  : 3    (10.3448275862%)
10) UNSUPPORTED CASE NUMBER : 3    (10.3448275862%)
11)SKIPPED TEST CASE NUMBER : 22    (75.8620689655%)

time = 2:
8) PASSED TEST CASE NUMBER  : 2    (8.69565217391%)
9) FAILED TEST CASE NUMBER  : 14    (60.8695652174%)
10) UNSUPPORTED CASE NUMBER : 7    (30.4347826087%)
11)SKIPPED TEST CASE NUMBER : 0    (0.0%)
```
* [10GMS: Reconfirm issue, transfer from DV-QuangNm][cHieu_confirm_issues_quangnm]
	- Setup system check issue with new fpga
		+ Just start action check normal path of issue: [AF6CCI0071-CEM-DV: Replace idle code was FAILED in case LOPs][AC1-I447]
		+ There is issue datapath, after run script, reload fpga 2,3 time current datapath ok.

### Plan

* Focus to finish the task: ```10GMS: Reconfirm issue, transfer from DV-QuangNm```

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [AF6CCI0071_10GMS_4.7_10.80_restore6]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005380091>

   [cHieu_confirm_issues_quangnm]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005413188>	 

   [AC1-I447]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005363281>
