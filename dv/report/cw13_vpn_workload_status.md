# Arrive Technologies

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Arrive Technologies](#arrive-technologies)
- [Estimate resource](#estimate-resource)
	- [Trinh Van Dang](#trinh-van-dang)
	- [Nguyen Van Bang](#nguyen-van-bang)
	- [Pham Minh Truong](#pham-minh-truong)
	- [Nguyen Minh Quang](#nguyen-minh-quang)
- [26 Mar, 2020](#26-mar-2020)
	- [Trinh Van Dang](#trinh-van-dang)
		- [Status](#status)
		- [Plan](#plan)
	- [Pham Minh Truong](#pham-minh-truong)
		- [Status](#status)
		- [Plan](#plan)
	- [Nguyen Minh Quang](#nguyen-minh-quang)
		- [Status](#status)
		- [Plan](#plan)
- [25 Mar, 2020](#25-mar-2020)
	- [Trinh Van Dang](#trinh-van-dang)
		- [Status](#status)
		- [Plan](#plan)
	- [Pham Minh Truong](#pham-minh-truong)
		- [Status](#status)
		- [Plan](#plan)
	- [Nguyen Minh Quang](#nguyen-minh-quang)
		- [Status](#status)
		- [Plan](#plan)
- [24 Mar, 2020](#24-mar-2020)
	- [Trinh Van Dang](#trinh-van-dang)
		- [Status](#status)
		- [Plan](#plan)
	- [Pham Minh Truong](#pham-minh-truong)
		- [Status](#status)
		- [Plan](#plan)
	- [Nguyen Minh Quang](#nguyen-minh-quang)
		- [Status](#status)
		- [Plan](#plan)
- [23 Mar, 2020](#23-mar-2020)
	- [Trinh Van Dang](#trinh-van-dang)
		- [Status](#status)
		- [Plan](#plan)
	- [Pham Minh Truong](#pham-minh-truong)
		- [Status](#status)
		- [Plan](#plan)
	- [Nguyen Minh Quang](#nguyen-minh-quang)
		- [Status](#status)
		- [Plan](#plan)

<!-- /TOC -->

# Estimate resource

## Trinh Van Dang

* Total workload: 100%
* Define mix test-cases for "CEM/Imsg application":
  - Finished: 50% task
* Full control QA for 10GMS cisco: List Sw items and transfer task for member and check it also. Check the new FPGA with update "interrupt restore", sum status, Support customer, ...
  - Plan: Finish it end of this week. Take about 35% workload.
  - Next release: Update interrupt restore based on the image fix CEM only (Cisco requested). Just move from 1-Apr to 6-Apr.
  - Take about 60% workload
* MRO 20G: Support aVC/Onder debug the ticket 101
  - Currently, I take about 5% workload to set-up/check on debug image.

## Nguyen Van Bang

* Total workload: To be define.
* He is helping to research "MACsec" Technologies. Currently he is sharing full workload on this task. BTW, I don't control this task, he is reporting to aMinh directly. Therefore, get his report for more inform task.

## Pham Minh Truong

* Total workload: 100%
* Share 20% to research MACsec
  - Get Bang's report for more inform this task.
* He's mainly working on 10GMS project. He is helping me to QA: interrupt restore, Pm/Fm, interrupt tree, mixing with TOH for next release.
  - Finish QA about 30% test-cases.
  - He's sharing 80% workload to QA this project.

## Nguyen Minh Quang

* Total workload: 105%
* Share 35% to research MACsec
  - Get Bang's report for more inform this task.
* He's mainly working on 10GMS project. He is helping me to QA: Smoke Traffic, Mixing test-cases for next release.  BTW, he's sharing his time to check/debug Imsg service test-case.
  - Finish QA about 80% test-cases for next release.
  - He's sharing 70% workload to QA this project.

# 26 Mar, 2020

## Trinh Van Dang

### Status

* Define mix test-cases for "CEM/Imsg application": added some Kbyte test-cases
	- 24 - 26 Mar: Nothing to update. Focus to QA 10GMS & 20GMS projects.
* 20G MRO:
	- Help aVC to debug the new image. Set-up check debug tool + Tried the test-case "Run traffic many times".
	- 24 Mar: a.VC just sent a new image today. That image was fixed the issue "run traffic many times". But, the timing has not well function. Therefore, a.VC will re-synt a new image to get timing better.
	- 25 Mar: a.VC just sent a new image with good timing this afternoon. I'm scanning it by autotest. It seems the status is good now. It's running ...
	- 26 Mar: Release the image to Ciena today. Waiting for Ciena confirm it. BTW, We will meeting with Onder when he duplicate it successfully.
* ATT_ETH_18G:
	- Support Hw/Sw to confirm all issues (~1 issues) assign to me.
* 10GMS Cisco:
	- Contact Hw/Sw to check some issues report from Quang
	- Sum status from Quang/Truong
		- The new FPGA to fix VT Interrupt restore issue still failed. We are still waiting for the new fpga...
		- aLongD/Quang still working to fix the Imsg issues.
* 10GMS Ciena: Support team to check some epass issues.

### Plan

* Define mix test-cases for "CEM/Imsg application"
* Help aVC to debug the new image fix the issue "Run traffic many times"
* Full control QA the project 10GMS Cisco.
* Support 10GMS Ciena check Epass issues (If have free time).

## Pham Minh Truong

### Status

* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore6
    - Continua test manual and build script to check automation
* Support Mr.Anh check new FPGA F6CCI0071_10GMS_4.7_10.80_restore8
    - Img was NOT FIXED issue, we will continua debug
		- https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005401210

### Plan

* Continua QA FPGA AF6CCI0071_10GMS_4.7_10.80_restore6
* Build automation test
* Take time to action task "MACsec"

## Nguyen Minh Quang

### Status
- Task: AF6CCI0071_10GMS_4.7_10.80_restore6: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005380091
		+ Status: Smoke traffic: DONE
							Mixing Satop: DONE
							Mixing CEP: Auto DONE, still analyze tomorrow (For more detail please check the files at the attachment)

- Reproduce is HA: AF6CNC1022-Mx-DV : Warm Restore was FAILED: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004693415
		+ Status: Still failed ===> aDinh will check tomorrow

- Support aLong to debug issue: AF6CCI0071-Imsg : Random encap channels Discard All Pkts: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005000092
		+ Status: Still not found root cause (for more detail please check task at the link: Support a.LongD to fix his remaining issues: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005402201)

- Support aKhuyen to debug issue: ATT_10G_MRO-DV: Force BIP error VC1x was FAILED: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000001176113/403027000005247007
		+ Status: assign to SW


### Plan

* Share time check the new FPGA to fix the issue “interrupt restore”. (Release to customer 6/4)
* Support HW/SW to debug remaining issue

# 25 Mar, 2020

## Trinh Van Dang

### Status

* Define mix test-cases for "CEM/Imsg application": added some Kbyte test-cases
	- 24, 25 Mar: Nothing to update. Focus to QA 10GMS & 20GMS projects.
* 20G MRO:
	- Help aVC to debug the new image. Set-up check debug tool + Tried the test-case "Run traffic many times".
	- 24 Mar: a.VC just sent a new image today. That image was fixed the issue "run traffic many times". But, the timing has not well function. Therefore, a.VC will re-synt a new image to get timing better.
	- 25 Mar: a.VC just sent a new image with good timing this afternoon. I'm scanning it by autotest. It seems the status is good now. It's running ...
* ATT_ETH_18G:
	- Support Hw/Sw to confirm all issues (~6 issues) assign to me.
* 10GMS:
	- Contact Hw/Sw to check some issues report from Quang
	- Sum status from Quang/Truong
		- The new FPGA to fix VT Interrupt restore issue still failed. We are still waiting for the new fpga...
		- aLongD/Quang still working to fix the Imsg issues.

### Plan

* Define mix test-cases for "CEM/Imsg application"
* Help aVC to debug the new image fix the issue "Run traffic many times"
* Full control QA the project 10GMS Cisco.
* Support 10GMS Ciena check Epass issues (If have free time).


## Pham Minh Truong

### Status

* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore6
    - Continua test manual and build script to check automation >>> TU3 is same happen issue "Interrupt restore just show 1 channel"
* Support Mr.Anh check new FPGA F6CCI0071_10GMS_4.7_10.80_restore7
    - Img was NOT FIXED issue, we will continua debug
		- https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005402142

### Plan

* Continua QA FPGA AF6CCI0071_10GMS_4.7_10.80_restore6
* Take time to action task "MACsec"

## Nguyen Minh Quang

### Status
- Task: AF6CCI0071_10GMS_4.7_10.80_restore6: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005380091
		+ Status: Smoke traffic: DONE
							Mixing Satop: DONE
							Mixing CEP: Auto still running.... (For more detail please check the files at the attachment)

- Support HW to debug issue: AF6CCI0071-DV-CEM: BERT engine not sync in case of Mixing CEM: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005375279
		+ Status: No RTLers join to debug ==> I take the system to run autotest mixing CEP  testcases

- Support aLong to debug issue: AF6CCI0071-Imsg : Random encap channels Discard All Pkts: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005000092
		+ Status: Still not found root cause (for more detail please check task at the link: Support a.LongD to fix his remaining issues: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005402201)

### Plan

* Share time check the new FPGA to fix the issue “interrupt restore”. (Release to customer 1/4)
* Support HW/SW to debug remaining issue

# 24 Mar, 2020

## Trinh Van Dang

### Status

* Define mix test-cases for "CEM/Imsg application": added some Kbyte test-cases
	- 24 Mar: Nothing to update. Focus to QA 10GMS & 20GMS projects.
* 20G MRO:
	- Help aVC to debug the new image. Set-up check debug tool + Tried the test-case "Run traffic many times".
	- 24 Mar: a.VC just sent a new image today. That image was fixed the issue "run traffic many times". But, the timing has not well function. Therefore, a.VC will re-synt a new image to get timing better.
* 10GMS:
	- Contact Hw/Sw to check some issues report from Quang
	- Help Cisco for some cases: B1 Error Notification from Arrive. Currently, We don't support it. Wait for Cisco request it or not.
	- Sum status from Quang/Truong
		- Truong found a urgent issue about interrupt restore. That issue is impacting to next release. Therefore, we are forcing RTL to debug it.

### Plan
* Define mix test-cases for "CEM/Imsg application"
* Help aVC to debug the new image fix the issue "Run traffic many times"
* Full control QA the project 10GMS Cisco.

## Pham Minh Truong

### Status

* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore6
    - Updated new result automation test last night (please check this link w:\projects\af6cci0071\working\autotest_report\QA_restore6\)
    - Found new SHOW STOPPER ISSUE "AF6CCI0071_DV_INT: Interrupt restore just show 1 channels vc1x"
        - Support Mr.Anh debug issue
        - https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005399077
    - Support Mr.Huynh check issue "AF6CCI0071_DV_INT: Some channels DS1 raise LOF when force full channels DS3 (5k channels)"
        - This issue is limit >>> noted and closed
        - https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#bugkey/403027000003095123/AC1-I439
    - Re-check and closed some old issue
        - AF6CCI0071_DV_Timing: Have issue when connect with JDSU >>> Closed
        - AF6CCI0071_DV_DCC: Counter MTU is not working >>> Processing
        - AF6CCI0071_DV_Interrupt: Interrupt restore is not working with prm-lbbit-change >>> Closed

### Plan

* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore6
* Take time to action task "MACsec"

## Nguyen Minh Quang

### Status
* 10GMS Cisco:
	- Task: AF6CCI0071_10GMS_4.7_10.80_restore6: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005380091
		+ Status: Smoke traffic: DONE (all good, please check file at the attachment)
			+ Mixing Satop: DONE (please check file analyze at the attachment)
			+ Mixing CEP: Auto still running.... (Will analyze ASAP: board is reserve to reproduce issue and let the aThanh check, Auto will run at the night and Analyze when it done)

	- Support HW to debug issue: AF6CCI0071-DV-CEM: BERT engine not sync in case of Mixing CEM: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005375279
		+ Status: Issue RTL, aAn Phuong will check ===> will continue tomorrow

	- Support aLong to debug issue: AF6CCI0071-Imsg : Random encap channels Discard All Pkts: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005000092
		+ Status: Still not found root cause ===> This task take more my workload
* MACsec:
  - Check Bang's report

### Plan

* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore6
* Take time to action task "MACsec"

# 23 Mar, 2020

## Trinh Van Dang

### Status

* Define mix test-cases for "CEM/Imsg application": added some Kbyte test-cases
* 20G MRO:
  - Help aVC to debug the new image. Set-up check debug tool + Tried the test-case "Run traffic many times"
* 10GMS:
  - Contact Hw/Sw to check some issues report from Quang
  - Help Cisco for some cases: B1 Error Notification from Arrive, V5.
  - Sum status from Quang/Truong.

### Plan
* Define mix test-cases for "CEM/Imsg application"
* Help aVC to debug the new image fix the issue "Run traffic many times"
* Full control QA the project 10GMS Cisco.

## Pham Minh Truong

### Status

* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore6
  - Analyzing testcase FAIL automation test  ---> Not found issue by design team, I will re-run with new update version auto test on tonight
  - Running INT TREE with interface STM64  ---> I found some basic issue, I'm trying replicate and report ASAP
  - If you want more detail, please check follow this link  w:\projects\af6cci0071\working\autotest_report\QA_restore6\

### Plan

* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore6
* Take time to action task "MACsec"

## Nguyen Minh Quang

### Status
* 10GMS Cisco:
  - [QA the new FPGA update interrupt restore] [AF6CCI0071_10GMS_4.7_10.80_restore6]
  ```sh
  Smoke traffic: DONE (all good, please check file at the attachment)
  Mixing Satop: DONE (please check file analyze at the attachment)
  Mixing CEP: Auto still running.... (Will analyze tomorrow)
  ```

  - Support HW to debug issue: AF6CCI0071-DV-CEM: BERT engine not sync in case of Mixing CEM
    -  Status: Need SW to check but no one available ===> will continue tomorrow (maybe) ===> This task take more my workload
  - Support aLong to debug issue: AF6CCI0071-Imsg : Random encap channels Discard All Pkts
    - Status: Still not found root cause ===> This task take more my workload
* MACsec:
  - Check Bang's report

### Plan
* Continua QA FPGA F6CCI0071_10GMS_4.7_10.80_restore6
* Take time to action task "MACsec"

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [AF6CCI0071_10GMS_4.7_10.80_restore6]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005380091>
