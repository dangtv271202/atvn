# <span style="color:Blue">Arrive Technologies</span>

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)

# 8 Apr, 2020
## Urgent issues
### 10GMS Cisco AF6CCI0071
1. [<span style="color:red">"device init" has not well functional][AC1-I451]
  - 30 Dec 2019: Quang raised this issue via mail but we must focus for CEM service on this phase. Therefore, set low priority.
  - 6 Apr: We just released the new image to update "CEM, Interrupt restore" today. Therefore, we should switch to next phase to fix Imsg issue and final this project. BTW, Cisco is testing Imsg on 10GMS project also, This issue should set to highest pri, because it's impacting to real application (Cisco IOS). That app is only run 'device init' in the first time.
  - 7 Apr: a.CThanh is using SW tool to compare configure.
  - 8 Apr: DV update disconnect XC on all IDs and try it again.
2. [<span style="color:red">[Ticket#9522] Serial interface not coming up with STS-48C/VC4-16C .][AC1-I450]
  - 8 Apr: Quang/aCThanh tried the CLI log (gen from API log, customer sent it) to reproduce it on diag version but not successfully. Therefore, need to HWer join to debug it on IOS version Cisco lab.
3. <span style="color:red">[AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]
  - 31 Mar: nganpdk said from 21/2 "next Monday, I will check again". But, we still have "no progress" in this issue.
  - 6 Apr: Ngan is analyzing it.
  - 7 Apr: Quang is creating the scripts to support Ngan debug it. BTW, he is busy to support check the issue ac1-i451. Therefore, he will add scripts and contact Ngan after finish that.
  - 8 Apr: Quang busy to check the customer issue. Therefore, he will be back at this work tomorrow.

## 10GMS Cisco AF6CCI0071
### Next release

* *Update FEAC*: ```5-May```
* *10GMS Fast, fix issue*: ???, @aNhan, please provide the plan.
* *Final image: Imsg/PPP + CEM*: ???, @aNhan, please provide the plan.


### Issues

#### external

* [Ticket#9522] Serial interface not coming up with STS-48C/VC4-16C .
  - 8 Apr: Quang/aCThanh tried the CLI log (gen from API log, customer sent it) to reproduce it on diag version but not successfully. Therefore, need to HWer join to debug it on IOS version Cisco lab.

#### Internal

* **<span style="color:green">HW/SW and DV are hard working last time. Many issues were fixed.**
* We just fixed the issue "interrupt restore" and official release to Cisco today.
* In this phase, we will create a plan to wrap-up this project with "CEM + Imsg/Ppp" service. Therefore, all issues should close. Please check Zoho link to cmt, create plan to fix it: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#bugsview/403027000003095123/6

## Ciena MRO 20G/10G with CAS

* [The ticket 101][20gmro_ticket_101], Info debug progress:
  * Ciena LAB: need reproduce issue with 250us JB so that dump buffer can capture enough info
  * Arrive: Van Cuong is adding logic to isolate wrong master STS configuration affect linklist storage (current design use this config as storage address) => plan release next debug image within this week
	* 10 Mar: Keep status, nothing to update.
	* 16 Mar: a.VC said "debug image route 2 ngay chua xong, chac add nhieu qua"
	* 17 Mar: *a.VC just sent a new image today. That image has not well function traffic when tried configure path many times (Change configure, not keep). aVC analyzed it and said that HO lost of Block. He will fix it soon*
	* 19 Mar: *a.VC sent a new image today to fix the issue "traffic has not well function when run many times". But, that fpga still failed.* AVC is analyzing more.
	* 20 Mar: Nothing to update.
	* 21-23 Mar: a.VC sent a new image to add debug tool. He checked it and found the root-cause of the issue "re-run traffic many times". He will fix it asap.
	* 24 Mar: a.VC just sent a new image today. That image was fixed the issue "run traffic many times". But, the timing has not well function. Therefore, a.VC will re-synt a new image to get timing better.
	* 25 Mar: a.VC just sent a new image with good timing this afternoon. I'm scanning it by autotest. It seems the status is good now. It's running ...
  * 26 Mar: We released the debug image to Ciena today. Waiting for Ciena confirm it
  * 27-31 Mar: Nothing to update
  * 6,8 Apr: Nothing to update.
* [The ticket 110][20gmro_ticket_110]
  * 30 Mar: Onder just reported this issue today. It seems it's an SDK issue. I reproduce it successfully in Arrive lab. aDinh is checking it
  * 31 Mar: <span style="color:green">We updated a new item "Fix STS192c CEP warm-start.". But, that item is impacting to a test-case from Ciena.That issue just fixed by the new sdk:/home/wdb/users/dv/dangtv/summary/ciena/sdk/autotest/epapp_panic. We will QA it and release path to Ciena tomorrow.
  * 6 Apr: Some "warm" issue are raising on automation test. Quang/aDinh is helping us to analyzing it.
  * 7 Apr: cTran just sent the SDK path to Ciena today. BTW, aDInh/Quang are checking more test-case with warm on autotest.
  * 8 Apr: As discussed via meeting, Warm will update by aNam for a new class python... Therefore, we will pause QA this project temporary and release all board for 10GMS team to speed-up QA.

# 7 Apr, 2020
## Urgent issues
### 10GMS Cisco AF6CCI0071
1. [<span style="color:red">"device init" has not well functional][AC1-I451]
  - 30 Dec 2019: Quang raised this issue via mail but we must focus for CEM service on this phase. Therefore, set low priority.
  - 6 Apr: We just released the new image to update "CEM, Interrupt restore" today. Therefore, we should switch to next phase to fix Imsg issue and final this project. BTW, Cisco is testing Imsg on 10GMS project also, This issue should set to highest pri, because it's impacting to real application (Cisco IOS). That app is only run 'device init' in the first time.
  - 7 Apr: a.CThanh is using SW tool to compare configure.
2. [<span style="color:red">AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406]
  - 13 Mar: @a.CThanh was updated SDK as a.LongD cmt but we tried it on-board not successfully. a.LongD will more check it.
  - 16, 17 Mar: Nothing to update.
  - 19 Mar: Issue discard pkt when unbind-bind service was FIXED, but have new issue: unbind-bind service affect other channels. Quang is working with aLong to fix it.
  - 23 Mar: Still waiting for aLong to fix it.
  - 24 - 26 Mar: Quang is working with a Long to find the root-cause.
  - 30 Mar: Nothing to update.
  - 31 Mar: a Long said that he is busy for other projects. Therefore, he will back to check this case about 15-Apr.
3. <span style="color:red">[AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]
  - 31 Mar: nganpdk said from 21/2 "next Monday, I will check again". But, we still have "no progress" in this issue.
  - 6 Apr: Ngan is analyzing it.
  - 7 Apr: Quang is creating the scripts to support Ngan debug it. BTW, he is busy to support check the issue ac1-i451. Therefore, he will add scripts and contact Ngan after finish that.

## 10GMS Cisco AF6CCI0071
### Next release

* *Update FEAC*: ```5-May```
* *10GMS Fast, fix issue*: ???, @aNhan, please provide the plan.
* *Final image: Imsg/PPP + CEM*: ???, @aNhan, please provide the plan.


### Issues

#### external

* [Ticket#9522] Serial interface not coming up with STS-48C/VC4-16C .
  - aCThanh is working with Cisco team to get API log. we will convert that log to CLI log and try it in Arrive lab.
  - Maybe it's the issue "device init 1 time has not well functional"

#### Internal

* **<span style="color:green">HW/SW and DV are hard working last time. Many issues were fixed.**
* We just fixed the issue "interrupt restore" and official release to Cisco today.
* In this phase, we will create a plan to wrap-up this project with "CEM + Imsg/Ppp" service. Therefore, all issues should close. Please check Zoho link to cmt, create plan to fix it: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#bugsview/403027000003095123/6

## Ciena MRO 20G/10G with CAS

* [The ticket 101][20gmro_ticket_101], Info debug progress:
  * Ciena LAB: need reproduce issue with 250us JB so that dump buffer can capture enough info
  * Arrive: Van Cuong is adding logic to isolate wrong master STS configuration affect linklist storage (current design use this config as storage address) => plan release next debug image within this week
	* 10 Mar: Keep status, nothing to update.
	* 16 Mar: a.VC said "debug image route 2 ngay chua xong, chac add nhieu qua"
	* 17 Mar: *a.VC just sent a new image today. That image has not well function traffic when tried configure path many times (Change configure, not keep). aVC analyzed it and said that HO lost of Block. He will fix it soon*
	* 19 Mar: *a.VC sent a new image today to fix the issue "traffic has not well function when run many times". But, that fpga still failed.* AVC is analyzing more.
	* 20 Mar: Nothing to update.
	* 21-23 Mar: a.VC sent a new image to add debug tool. He checked it and found the root-cause of the issue "re-run traffic many times". He will fix it asap.
	* 24 Mar: a.VC just sent a new image today. That image was fixed the issue "run traffic many times". But, the timing has not well function. Therefore, a.VC will re-synt a new image to get timing better.
	* 25 Mar: a.VC just sent a new image with good timing this afternoon. I'm scanning it by autotest. It seems the status is good now. It's running ...
  * 26 Mar: We released the debug image to Ciena today. Waiting for Ciena confirm it
  * 27-31 Mar: Nothing to update
  * 6,7 Apr: Nothing to update.
* [The ticket 110][20gmro_ticket_110]
  * 30 Mar: Onder just reported this issue today. It seems it's an SDK issue. I reproduce it successfully in Arrive lab. aDinh is checking it
  * 31 Mar: <span style="color:green">We updated a new item "Fix STS192c CEP warm-start.". But, that item is impacting to a test-case from Ciena.That issue just fixed by the new sdk:/home/wdb/users/dv/dangtv/summary/ciena/sdk/autotest/epapp_panic. We will QA it and release path to Ciena tomorrow.
  * 6 Apr: Some "warm" issue are raising on automation test. Quang/aDinh is helping us to analyzing it.
  * 7 Apr: cTran just sent the SDK path to Ciena today. BTW, aDInh/Quang are checking more test-case with warm on autotest.


# 6 Apr, 2020
## Urgent issues
### 10GMS Cisco AF6CCI0071
1. <span style="color:red">"device init" has not well functional</span>
  - 30 Dec 2019: Quang raised this issue via mail but we must focus for CEM service on this phase. Therefore, set low priority.
  - 6 Apr: We just released the new image to update "CEM, Interrupt restore" today. Therefore, we should switch to next phase to fix Imsg issue and final this project. BTW, Cisco is testing Imsg on 10GMS project also, This issue should set to highest pri, because it's impacting to real application (Cisco IOS). That app is only run 'device init' in the first time.
2. [<span style="color:red">AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406]
  - 13 Mar: @a.CThanh was updated SDK as a.LongD cmt but we tried it on-board not successfully. a.LongD will more check it.
  - 16, 17 Mar: Nothing to update.
  - 19 Mar: Issue discard pkt when unbind-bind service was FIXED, but have new issue: unbind-bind service affect other channels. Quang is working with aLong to fix it.
  - 23 Mar: Still waiting for aLong to fix it.
  - 24 - 26 Mar: Quang is working with a Long to find the root-cause.
  - 30 Mar: Nothing to update.
  - 31 Mar: a Long said that he is busy for other projects. Therefore, he will back to check this case about 15-Apr.
3. <span style="color:red">[AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]
  - 31 Mar: nganpdk said from 21/2 "next Monday, I will check again". But, we still have "no progress" in this issue.
  - 6 Apr: Ngan is analyzing it.
4. <span style="color:red">[AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345]
  - 6 Apr: Khoa said "Because workloed for other task . i will check this isuee within 2  next weeks".

## 10GMS Cisco AF6CCI0071
### Next release

* *Update FEAC*: ```5-May```
* *10GMS Fast, fix issue*: ???, @aNhan, please provide the plan.
* *Final image: Imsg/PPP + CEM*: ???, @aNhan, please provide the plan.


### Issues

#### external

* [Ticket#9522] Serial interface not coming up with STS-48C/VC4-16C .
  - aCThanh is working with Cisco team to get API log. we will convert that log to CLI log and try it in Arrive lab.
  - Maybe it's the issue "device init 1 time has not well functional"

#### Internal

* **<span style="color:green">HW/SW and DV are hard working last time. Many issues were fixed.**
* We just fixed the issue "interrupt restore" and official release to Cisco today.
* In this phase, we will create a plan to wrap-up this project with "CEM + Imsg/Ppp" service. Therefore, all issues should close. Please check Zoho link to cmt, create plan to fix it: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#bugsview/403027000003095123/6

## Ciena MRO 20G/10G with CAS

* [The ticket 101][20gmro_ticket_101], Info debug progress:
  * Ciena LAB: need reproduce issue with 250us JB so that dump buffer can capture enough info
  * Arrive: Van Cuong is adding logic to isolate wrong master STS configuration affect linklist storage (current design use this config as storage address) => plan release next debug image within this week
	* 10 Mar: Keep status, nothing to update.
	* 16 Mar: a.VC said "debug image route 2 ngay chua xong, chac add nhieu qua"
	* 17 Mar: *a.VC just sent a new image today. That image has not well function traffic when tried configure path many times (Change configure, not keep). aVC analyzed it and said that HO lost of Block. He will fix it soon*
	* 19 Mar: *a.VC sent a new image today to fix the issue "traffic has not well function when run many times". But, that fpga still failed.* AVC is analyzing more.
	* 20 Mar: Nothing to update.
	* 21-23 Mar: a.VC sent a new image to add debug tool. He checked it and found the root-cause of the issue "re-run traffic many times". He will fix it asap.
	* 24 Mar: a.VC just sent a new image today. That image was fixed the issue "run traffic many times". But, the timing has not well function. Therefore, a.VC will re-synt a new image to get timing better.
	* 25 Mar: a.VC just sent a new image with good timing this afternoon. I'm scanning it by autotest. It seems the status is good now. It's running ...
  * 26 Mar: We released the debug image to Ciena today. Waiting for Ciena confirm it
  * 27-31 Mar: Nothing to update
  * 6 Apr: Nothing to update.
* [The ticket 110][20gmro_ticket_110]
  * 30 Mar: Onder just reported this issue today. It seems it's an SDK issue. I reproduce it successfully in Arrive lab. aDinh is checking it
  * 31 Mar: <span style="color:green">We updated a new item "Fix STS192c CEP warm-start.". But, that item is impacting to a test-case from Ciena.That issue just fixed by the new sdk:/home/wdb/users/dv/dangtv/summary/ciena/sdk/autotest/epapp_panic. We will QA it and release path to Ciena tomorrow.
  * 6 Apr: Some "warm" issue are raising on automation test. Quang/aDinh is helping us to analyzing it.

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [AC1-I451]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005457481>
   [AC1-I450]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005448380>
   [AC1-I449]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005399077>
   [AC1-I448]: <https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005375279>
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
