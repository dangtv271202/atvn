# <span style="color:Blue">Arrive Technologies</span>

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)



# 31 Mar, 2020
## Urgent issues
### 10GMS Cisco AF6CCI0071
1. [<span style="color:red">AF6CCI0071_DV_INT: Interrupt restore just show 1 channels vc1x</span>][AC1-I449]
  - 24 Mar: This issue is impacting to next release. Therefore, ee are setting "show stopper" issue. aTAnh said that "he found the root-cause". Wait for aTNhan to re-synt a new image ....
  - 25 Mar: <span style="color:red">a.TAnh just sent a new FPGA today to fix this issue but that image was failed. Therefore, we are waiting for the new FPGA to fix it...</span>
  - 26 Mar: <span style="color:red">The new image still was failed. Continue waiting for the new image ...</span>
  - 27-31 Mar: <span style="color:green">It seems fixed by the new FPGA restore_09. Truong is more checking it.
2. [<span style="color:red">AF6CCI0071-DV-CEM: Loopback Tu3 was FAILED  in case of Mixing CEM</span>][AC1-I448]
  - 18 Mar: Need to Hw check it.
  - 19, 20 Mar: Nothing to update. (Still waiting for Hwer ...)
  - 23 Mar: Ngan/Quang checked it today: "Maybe issue is impacting by tu3 loopback". <span style="color:red">Therefore, need to *SW team* share time to check it</span>.
  - 24 Mar: a.Chi Thanh shared time to check this case today and saw that it's a Hw issue. Need to a.An Phuong share time to check it.
  - 25-30 Mar: <span style="color:red">Nothing to update. Hw is doesn't activated yet.</span>
  - 31 Mar: <span style="color:green">An Phuong said that he just update RTL code to fix this case. Therefore, waiting for a nhanngt to release the new image ...
3. [<span style="color:red">AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406]
  - 13 Mar: @a.CThanh was updated SDK as a.LongD cmt but we tried it on-board not successfully. a.LongD will more check it.
  - 16, 17 Mar: Nothing to update.
  - 19 Mar: Issue discard pkt when unbind-bind service was FIXED, but have new issue: unbind-bind service affect other channels. Quang is working with aLong to fix it.
  - 23 Mar: Still waiting for aLong to fix it.
  - 24 - 26 Mar: Quang is working with a Long to find the root-cause.
  - 30 Mar: Nothing to update.
  - 31 Mar: a Long said that he is busy for other projects. Therefore, he will back to check this case about 15-Apr.
4. <span style="color:red">H.C.Thanh is busy to bring-up new project Raise-Com. Therefore, some issues were paused debugging.</span>
  - 13 - 26 Mar: <span style="color:red">Nothing to update. Hw is doesn't activated yet.</span>
  - 27 Mar: Thanh.H.C contacted Quang to get more inform. Wait for the new fpga to fix these issues.
  - 30 Mar: Nothing to update.
  - 31 Mar: aNhan just sent the new FPGA to fix some issues of CThanh. The result as below:
    + Added PTCH, detect DA type failed -> <span style="color:red">still failed. Need to CThanh recheck it
    + Broadcast counter -> <span style="color:green">Fixed.
5. <span style="color:red">[AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]
  - 31 Mar: nganpdk said from 21/2 "next Monday, I will check again". But, we still have "no progress" in this issue.

## 10GMS Cisco AF6CCI0071
### Next release

* *10GMS not fast, fix issue*: 6-Apr (old plan: 1-Apr)
* *10GMS Fast, fix issue*: ???, @aNhan, please provide the plan.


### Issues

#### external

Nothing to update.

#### Internal

* @a.Nha^n/Dung: Please check and assign issue to member. <span style="color:red">Many issues do not have a plan or a comment to solve. Please check on Zoho issue list. BTW, Cisco is testing IMSG service. Many Issues are pause debug in the Arrive lab. Please create a plan to fix it.
* **Some critical/show stopper issues: (it's marking on Zoho)**.

|Issue Prefix |Titile |Assignee - Email|
| ------ | ------ | ------ |
| AC1-I448 | [AF6CCI0071-DV-CEM: Loopback Tu3 was FAILED  in case of Mixing CEM][AC1-I448] | nhanngt@atvn.com.vn |
| AC1-I406 | [AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406] | thanhnc@atvn.com.vn |
| AC1-I345 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | khoams@atvn.com.vn |
| AC1-I328 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn |
| AC1-I324 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn |
| AC1-I279 | [AF6CCI0071_DV_Intterupt: Intterupt restore not working][AC1-I279] | nhanngt@atvn.com.vn |
| AC1-I253 | [AF6CCi0071-Mx-DV : LOPState and LOPSyn is the same][AC1-I253] | nhanngt@atvn.com.vn |
| AC1-I186 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn |
| AC1-I172 | [AF6CCI0071_DV_PDA: Lost block PDA when change many datapath][AC1-I172] | longdt@atvn.com.vn |
| AC1-I136 | [AF6CCI0071-iMS-Mx-DV-PPP-OverBW: Behavior of overBW not correct][AC1-I136] | longdt@atvn.com.vn |


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
* [The ticket 110][20gmro_ticket_110]
  * 30 Mar: Onder just reported this issue today. It seems it's an SDK issue. I reproduce it successfully in Arrive lab. aDinh is checking it
  * 31 Mar: <span style="color:green">We updated a new item "Fix STS192c CEP warm-start.". But, that item is impacting to a test-case from Ciena.That issue just fixed by the new sdk:/home/wdb/users/dv/dangtv/summary/ciena/sdk/autotest/epapp_panic. We will QA it and release path to Ciena tomorrow.


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

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
