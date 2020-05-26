# Arrive Technologies

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)


# Estimate resource

## Trinh Van Dang

* Total workload: ```>100%```
* Full control QA for 10GMS cisco: List Sw items and transfer task for member and check it also. Check the new FPGA with update "interrupt restore", sum status, Support customer, ...
  - Next release: Update FEAC ```5 May```
  - Wrap-up this project with ```CEM + Imsg/Ppp```: Plan ```TBD```
  - Take about ```75% workload```
* MRO 20G: Full control QA for this project
	- Ticket 101: Support aVC/Onder to debug this issue
	- Ticket 110: Support aDinh/Onder to fix it.
  - Sum status, issue
	- Take about ```15% workload```
* 10GMS Ciena AF6CNC0071: Support c.Hoa's team to confirm some Epass issues. Take about ```1% workload```
* ATT_ETH_18G/ATT: Confirm some issues from SW/HW. Take about ```15% workload```

## Nguyen Van Bang

* Total workload: ```To be define.```
* He is helping to research "MACsec" Technologies. Currently he is sharing full workload on this task. BTW, I don't control this task, he is reporting to aMinh directly. Therefore, get his report for more inform task.

## Pham Minh Truong

* Total workload: ```>100%```
* He's mainly working on 10GMS project. He is helping me to QA: interrupt restore, Pm/Fm, interrupt tree, DCC, mixing with TOH for next release. BTW he help me to run, support and analyze the new auto-test support ```PM for Mixing```.
  - He's sharing ```100% workload``` to QA this project.
* Other tasks: Support ATT team to confirm issue, ... ```TBD```

## Nguyen Minh Quang

* Total workload: ```> 100%```
* He's mainly working on 10GMS project. In this phase, we hope to wrap-up this projects. Therefore, many imgs issues should close. So, Quang will take more time to help us finish that.
  - He's sharing ```85% workload``` to QA this project.
* 20G MRO: Support aDinh to update "warm restore" on this project. ```He takes about 22% workload```

# 8 Apr, 2020

## Trinh Van Dang

### Status
* Take time (10-11h30 AM) to join meeting to discuss "warm" with aQC, aDinh, aNam, aMinh,... today.
* Define mix test-cases for "CEM/Imsg application": added some Kbyte test-cases
	- 30 Mar: ```Finished```. Wait for a.Minh to review it.
  - 31 Mar: Meeting with a Minh and team for this topic (from 3h PM: 4h PM). About my task, I will update:
    + Interrupt flooding: Update interrupt soaking
    + OH over PSN: Update more test-case and detail pass condition.
    + Hope finish it tomorrow.
  - 1 Apr-6 Apr: I was finished this task. Wait for aMinh review it.
  - 7 Apr: Today I taken about 2h to meeting with team to review test-case of aKhanh/cHoa/cMai. Hope review my task on tomorrow.
  - 8 Apr: aMinh takes times (3-5h PM) to review it today. He comments some cases and I just finished update as he requested. This task was done.
* 20G MRO:
	- Warm failed with some cases on autotest. Quang/aDinh is analyzing it.
  - 7 Apr: Pause testing it today, we are focusing for 10GMS project.
  - 8 Apr: As discussed via meeting, aNam will improve a class for autotest... Therefore ww will pause QA this project temporary and release board for 10GMS team to speed-up QA.
* 10GMS Cisco:
  - We are focusing for this project today and working on many issues:
    + [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451]
      ++ Debug with aCThanh/Quang: update auto with disconnect all XC and try again.
      ++ For customer issue, Quang tried with the CLI log with diag board and gen OAM traffic from ARAD but not reproduce it. Maybe, need to HW join to debug with IOS system in Cisco lab.
  - BTW, We are running autotest for PM, interrupt restore,... for this project.
  - Check item update on the new SDK.
* 10GMS Ciena:
  - Support team for many epass issues (aNha^n/QC request).

### Plan

* Full control QA the project ```10GMS Cisco```.
* Support 10GMS Ciena check Epass issues (If request).
* Confirm some issue on ATT projects (If Hw/SW fix it).

## Pham Minh Truong

### Status


* Check new option update at new SDK 4.5.0.b000
    - Update to cache database of jitter buffer and delay when setting jitterbuffer/delay more correctly to fix HA issue >>> It's working correctly
    - https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005479274
* Continua run and check new function automation test  PM functional
    - At pw mixing, happen issue STUCK when run normal mixing traffic ---> I'm analyze and compare with old FPGA
    - SDH mixing, counter always count NEG/DEG gen because not same timing between DUT and ATT ---> I'm asking Mr.Minh for new solution

### Plan

*  Action new task "support auto-test to support "PM cho mixing voi cac layer line, HO, LO, DE3, DE1 va PW""

## Nguyen Minh Quang

### Status

- Task: 4.5.0.b000: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005479274
    + Status: DONE

- Support HW/SW to debug issue: AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005457481
    + Status: Auto-test disconnect not full channels ---> wait aMinh update auto-test and re-run

- Task: [Ticket#9522] Serial interface not coming up with STS-48C/VC4-16C: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005448374
    + Status: The script worked well with mode diag ====> Need try it on IOS system

### Plan

* 10GMS Cisco: Debug with Hw/Sw to fix remain issues on Zoho. Hope wrap-up this project. He is focusing for Imsg service.


# 7 Apr, 2020

## Trinh Van Dang

### Status
* Define mix test-cases for "CEM/Imsg application": added some Kbyte test-cases
	- 30 Mar: ```Finished```. Wait for a.Minh to review it.
  - 31 Mar: Meeting with a Minh and team for this topic (from 3h PM: 4h PM). About my task, I will update:
    + Interrupt flooding: Update interrupt soaking
    + OH over PSN: Update more test-case and detail pass condition.
    + Hope finish it tomorrow.
  - 1 Apr-6 Apr: I was finished this task. Wait for aMinh review it.
  - 7 Apr: Today I taken about 2h to meeting with team to review test-case of aKhanh/cHoa/cMai. Hope review my task on tomorrow.
* 20G MRO:
	- Warm failed with some cases on autotest. Quang/aDinh is analyzing it.
  - 7 Apr: Pause testing it today, we are focusing for 10GMS project.
* 10GMS Cisco:
  - We are focusing for this project today and working on many issues:
    + [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451]
      ++ This is a urgent issue. aCThanh is using tool to compare configure. Quang is helping us on this.
    + AF6CCi0071-Mx-DV : TOH_PW-Can not force alarm L/Rbit: Truong confirmed it and closed this issue.
    + AF6CCI0071_DV_DCC: Eth port count both param rxUndersizePackets and rxPacketsLen64: Truong confirmed it and closed this issue.
  - BTW, We are running autotest for PM, interrupt restore,... for this project.
* 10GMS Ciena:
  - Support team for many epass issues.

### Plan

* Wait for aMinh review "mix test-cases for ```CEM/Imsg application```"
* Help aDinh/Onder debug the ```ticket 110``` on MRO project.
* Full control QA the project ```10GMS Cisco```.
* Support 10GMS Ciena check Epass issues (If request).
* Confirm some issue on ATT projects (If Hw/SW fix it).

## Pham Minh Truong

### Status

* Re-check some old issue
    - AF6CCi0071-Mx-DV : TOH_PW-Can not force alarm L/Rbit
        + Re-check with lasted version >>> Issue was FIXED
        + https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004442001
    - AF6CCI0071_DV_DCC: Eth port count both param rxUndersizePackets and rxPacketsLen64
        + Re-check with lasted version >>> Issue was FIXED
        + https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004602311
* Continua run and analyze automation test about mixing, interrupt restore functional

### Plan

* Action new task "support auto-test to support "PM cho mixing voi cac layer line, HO, LO, DE3, DE1 va PW""

## Nguyen Minh Quang

### Status

- Support HW/SW to debug issue: AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005457481
    + Status: wait aThanh update status

- Task: AF6CCI0071_10GMS_4.7_10.80_restore10(smoke CEM and Imsg traffic): https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005430089
    + Status: DONE

### Plan

* 20G MRO: Help to scan warm test-case
* 10GMS Cisco: Debug with Hw/Sw to fix remain issues on Zoho. Hope wrap-up this project.

# 6 Apr, 2020

## Trinh Van Dang

### Status

* Define mix test-cases for "CEM/Imsg application": added some Kbyte test-cases
	- 30 Mar: ```Finished```. Wait for a.Minh to review it.
  - 31 Mar: Meeting with a Minh and team for this topic (from 3h PM: 4h PM). About my task, I will update:
    + Interrupt flooding: Update interrupt soaking
    + OH over PSN: Update more test-case and detail pass condition.
    + Hope finish it tomorrow.
  - 1 Apr-6 Apr: I was finished this task. Wait for aMinh review it.
* 20G MRO:
	- Warm failed with some cases on autotest. Quang/aDinh is analyzing it.
* 10GMS Cisco:
	- We just sent official release the new FPGA to update "interrupt restore" to Cisco today. DV is scanning it more.
  - DV team is working with Hw/SW to fix all issues on Zoho link.
* ATT_ETH_18G: Confirm an issue on zoho with the new FPGA. but, that image was failed, the traffic has not well functional. Wait for Hw to check it.
* ATT_6a210081: Currently the FPGA and SDK are not sync, we must force product code to run it. That is not safe, I'm not sure traffic is Ok after force and any developer join to check it. Therefore, I re-assign it to SW team to update SDK for that case first.

### Plan

* Wait for aMinh review "mix test-cases for ```CEM/Imsg application```"
* Help aDinh/Onder debug the ```ticket 110``` on MRO project.
* Full control QA the project ```10GMS Cisco```.
* Support 10GMS Ciena check Epass issues (If request).
* Confirm some issue on ATT projects (If Hw/SW fix it).

## Pham Minh Truong

### Status

This is his report. I think he is very hard work last time:

* Continua run automation test, analyze and support Mr.Minh fixed some error
    - Automation test is available to running
    - Check and analyze some test case FAILED (was fixed with new version automation)

* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore10
    - I'm run automation test for scanning interrupt restore

### Plan

* Still QA on the project 10GMS: interrupt restore, Pm/Fm, interrupt tree, DCC, mixing with TOH for next release. BTW he help me to run, support and analyze the new auto-test support ```PM for Mixing```.


## Nguyen Minh Quang

### Status

* He is very hard work today. He shared more time to debug with HWer (Ngan, LongD) and SWer (aDInh, aCThanh) on many projects: 20G MRO, 10GMS.
* Support aDinh to check warm functional on 20G MRO project.
* 10GMS:
  - Task: [Ticket#9522] Serial interface not coming up with STS-48C/VC4-16C: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005448374
      + Status: need logger from Cisco to reproduce

  - Task: AF6CCI0071_10GMS_4.7_10.80_restore10(smoke CEM and Imsg traffic): https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005430089
      + Status: Auto-test still running (please check the link for detail)

  - Support aNgan to debug issue: AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004542007
      + Status: aNgan still debug

  - Task: Add/update result test-case CEM mixing to sync with autotest support: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005259044
      + Status: DONE

### Plan

* 20G MRO: Help to scan warm test-case
* 10GMS Cisco: Debug with Hw/Sw to fix remain issues on Zoho. Hope wrap-up this project.


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [AF6CCI0071_10GMS_4.7_10.80_restore6]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005380091>

   [cHieu_confirm_issues_quangnm]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005413188>	 

      [AC1-I449]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005399077>
      [AC1-I448]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005375279>
      [AC1-I447]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005363281>
      [AC1-I415]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005075062>
      [AC1-I406]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005000092>
      [AC1-I345]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004614259>
      [AC1-I328]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004546009>
      [AC1-I324]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004542007>
      [AC1-I279]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004274103>
      [AC1-I253]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004274103>
      [AC1-I186]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004048184>
      [AC1-I172]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004020719>
      [AC1-I136]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000003933388>

      [20gmro_ticket_101]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000000038143/403027000004562009/403027000005373041>
      [20gmro_ticket_110]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000000038143/403027000005413344>
