# <span style="color:Blue">Arrive Technologies</span>

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)



# 26 Mar, 2020
## Urgent issues
### 10GMS Cisco AF6CCI0071
1. [<span style="color:red">AF6CCI0071_DV_INT: Interrupt restore just show 1 channels vc1x</span>][AC1-I449]
  - 24 Mar: This issue is impacting to next release. Therefore, ee are setting "show stopper" issue. aTAnh said that "he found the root-cause". Wait for aTNhan to re-synt a new image ....
	- 25 Mar: <span style="color:red">a.TAnh just sent a new FPGA today to fix this issue but that image was failed. Therefore, we are waiting for the new FPGA to fix it...</span>
  - 26 Mar: <span style="color:red">The new image still was failed. Continue waiting for the new image ...</span>
2. [<span style="color:red">AF6CCI0071-DV-CEM: Loopback Tu3 was FAILED  in case of Mixing CEM</span>][AC1-I448]
	- 18 Mar: Need to Hw check it.
	- 19, 20 Mar: Nothing to update. (Still waiting for Hwer ...)
	- 23 Mar: Ngan/Quang checked it today: "Maybe issue is impacting by tu3 loopback". <span style="color:red">Therefore, need to *SW team* share time to check it</span> .
	- 24 Mar: a.Chi Thanh shared time to check this case today and saw that it's a Hw issue. Need to a.An Phuong share time to check it.
	- 25-26 Mar: <span style="color:red">Nothing to update. Hw is doesn't activated yet.</span>
3. [<span style="color:red">AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406]
  - 13 Mar: @a.CThanh was updated SDK as a.LongD cmt but we tried it on-board not successfully. a.LongD will more check it.
  - 16, 17 Mar: Nothing to update.
  - 19 Mar: Issue discard pkt when unbind-bind service was FIXED, but have new issue: unbind-bind service affect other channels. Quang is working with aLong to fix it.
  - 23 Mar: Still waiting for aLong to fix it.
  - 24 - 26 Mar: Quang is working with a Long to find the root-cause.
4. [<span style="color:red">AF6CCI0071-Mx-DV : PPP: VC3 over BW with cfg = 65,595bytes(92% BW)][AC1-I415]
  - 23 Mar: This issue  was reported a long time ago. We can't run full BW for Imsg service. Need to Hw share time to check it.
  - 24,25 Mar: <span style="color:red">Nothing to update. Hw is doesn't activated yet.</span>
5. <span style="color:red">H.C.Thanh is busy to bring-up new project Raise-Com. Therefore, some issues were paused debugging.</span>
  - 13 - 26 Mar: <span style="color:red">Nothing to update. Hw is doesn't activated yet.</span>

## 10GMS Cisco AF6CCI0071
### Next release

* *10GMS not fast, fix issue*: 6-Apr (old plan: 1-Apr)
* *10GMS Fast, fix issue*: ???, @aNhan, please provide the plan.


### Issues

#### external

Nothing to update.

#### Internal

* @a.Nha^n/Dung: Please check and assign issue to member. <span style="color:red">Many issues do not have a plan or a comment to solve. Please check on Zoho issue list.
* **Some critical/show stopper issues: (it's marking on Zoho)**.

|Issue Prefix |Titile |Assignee - Email|
| ------ | ------ | ------ |
| AC1-I449 | [AF6CCI0071_DV_INT: Interrupt restore just show 1 channels vc1x][AC1-I449] | anhht@atvn.com.vn |
| AC1-I448 | [AF6CCI0071-DV-CEM: Loopback Tu3 was FAILED  in case of Mixing CEM][AC1-I448] | phuongna@atvn.com.vn |
| AC1-I415 | [AF6CCI0071-Mx-DV : PPP: VC3 over BW with cfg = 65,595bytes(92% BW)][AC1-I415] | nhanngt@atvn.com.vn |
| AC1-I406 | [AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406] | thanhnc@atvn.com.vn |
| AC1-I345 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | truongpm@atvn.com.vn |
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


# 25 Mar, 2020
## Urgent issues
### 10GMS Cisco AF6CCI0071
1. [<span style="color:red">AF6CCI0071_DV_INT: Interrupt restore just show 1 channels vc1x</span>][AC1-I449]
  - 24 Mar: This issue is impacting to next release. Therefore, ee are setting "show stopper" issue. aTAnh said that "he found the root-cause". Wait for aTNhan to re-synt a new image ....
	- 25 Mar: <span style="color:red">a.TAnh just sent a new FPGA today to fix this issue but that image was failed. Therefore, we are waiting for the new FPGA to fix it...</span>
2. [<span style="color:red">AF6CCI0071-DV-CEM: Loopback Tu3 was FAILED  in case of Mixing CEM</span>][AC1-I448]
	- 18 Mar: Need to Hw check it.
	- 19, 20 Mar: Nothing to update. (Still waiting for Hwer ...)
	- 23 Mar: Ngan/Quang checked it today: "Maybe issue is impacting by tu3 loopback". <span style="color:red">Therefore, need to *SW team* share time to check it</span> .
	- 24 Mar: a.Chi Thanh shared time to check this case today and saw that it's a Hw issue. Need to a.An Phuong share time to check it.
	- 25 Mar: <span style="color:red">Nothing to update. Hw is doesn't activated yet.</span>
3. [<span style="color:red">AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406]
  - 13 Mar: @a.CThanh was updated SDK as a.LongD cmt but we tried it on-board not successfully. a.LongD will more check it.
  - 16, 17 Mar: Nothing to update.
  - 19 Mar: Issue discard pkt when unbind-bind service was FIXED, but have new issue: unbind-bind service affect other channels. Quang is working with aLong to fix it.
  - 23 Mar: Still waiting for aLong to fix it.
  - 24,25 Mar: Quang is working with a Long to find the root-cause.
4. [<span style="color:red">AF6CCI0071-Mx-DV : PPP: VC3 over BW with cfg = 65,595bytes(92% BW)][AC1-I415]
  - 23 Mar: This issue  was reported a long time ago. We can't run full BW for Imsg service. Need to Hw share time to check it.
  - 24,25 Mar: <span style="color:red">Nothing to update. Hw is doesn't activated yet.</span>
5. <span style="color:red">H.C.Thanh is busy to bring-up new project Raise-Com. Therefore, some issues were paused debugging.</span>
  - 13 - 25 Mar: <span style="color:red">Nothing to update. Hw is doesn't activated yet.</span>

## 10GMS Cisco AF6CCI0071
### Next release

* *10GMS not fast, fix issue*: 6-Apr (old plan: 1-Apr)
* *10GMS Fast, fix issue*: ???, @aNhan, please provide the plan.


### Issues

#### external

Nothing to update.

#### Internal

* @a.Nha^n/Dung: Please check and assign issue to member. <span style="color:red">Many issues do not have a plan or a comment to solve. Please check on Zoho issue list.
* **Some critical/show stopper issues: (it's marking on Zoho)**.

|Issue Prefix |Titile |Assignee - Email|
| ------ | ------ | ------ |
| AC1-I449 | [AF6CCI0071_DV_INT: Interrupt restore just show 1 channels vc1x][AC1-I449] | anhht@atvn.com.vn |
| AC1-I448 | [AF6CCI0071-DV-CEM: Loopback Tu3 was FAILED  in case of Mixing CEM][AC1-I448] | phuongna@atvn.com.vn |
| AC1-I415 | [AF6CCI0071-Mx-DV : PPP: VC3 over BW with cfg = 65,595bytes(92% BW)][AC1-I415] | nhanngt@atvn.com.vn |
| AC1-I406 | [AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406] | thanhnc@atvn.com.vn |
| AC1-I345 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | truongpm@atvn.com.vn |
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

# 24 Mar, 2020
## Urgent issues
### 10GMS Cisco AF6CCI0071
1. [<span style="color:red">AF6CCI0071_DV_INT: Interrupt restore just show 1 channels vc1x</span>][AC1-I449]
  - 24 Mar: This issue is impacting to next release. Therefore, ee are setting "show stopper" issue. aTAnh said that "he found the root-cause". Wait for aTNhan to re-synt a new image ....
2. [<span style="color:red">AF6CCI0071-DV-CEM: Loopback Tu3 was FAILED  in case of Mixing CEM</span>][AC1-I448]
  - 18 Mar: Need to Hw check it.
  - 19, 20 Mar: Nothing to update. (Still waiting for Hwer ...)
  - 23 Mar: Ngan/Quang checked it today: "Maybe issue is impacting by tu3 loopback". <span style="color:red">Therefore, need to *SW team* share time to check it</span> .
  - 24 Mar: a.Chi Thanh shared time to check this case today and saw that it's a Hw issue. Need to a.An Phuong share time to check it.
3. [<span style="color:red">AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406]
  - 13 Mar: @a.CThanh was updated SDK as a.LongD cmt but we tried it on-board not successfully. a.LongD will more check it.
  - 16, 17 Mar: Nothing to update.
  - 19 Mar: Issue discard pkt when unbind-bind service was FIXED, but have new issue: unbind-bind service affect other channels. Quang is working with aLong to fix it.
  - 23 Mar: Still waiting for aLong to fix it.
  - 24 Mar: Quang is working with a Long to find the root-cause.
4. [<span style="color:red">AF6CCI0071-Mx-DV : PPP: VC3 over BW with cfg = 65,595bytes(92% BW)][AC1-I415]
  - 23 Mar: This issue  was reported a long time ago. We can't run full BW for Imsg service. Need to Hw share time to check it.
  - 24 Mar: Nothing to update. Hw is doesn't activated yet.
5. <span style="color:red">H.C.Thanh is busy to bring-up new project Raise-Com. Therefore, some issues were paused debugging.</span>
  - 13 - 24 mar: Nothing to update.

## 10GMS Cisco AF6CCI0071
### Next release

* *10GMS not fast, fix issue*: 6-Apr (old plan: 1-Apr)
* *10GMS Fast, fix issue*: ???, @aNhan, please provide the plan.


### Issues

#### external

* Cisco is asking a question about "B1 Error Notification from Arrive".
  - 23 Mar: Need to a.TAnh share time to feedback it.
  - Feedback to Cisco:

    On 3/24/2020 4:30 PM, Dhamodharan Krishnamurthy -X (dhakrish - HCL TECHNOLOGIES LIMITED at Cisco) wrote:
  >
  > Hi Dang,
  >
  >  
  >
  > Thanks for the update.
  >
  >  
  >
  > Regards,
  >
  > Dhamo
  >
  >  
  >
  > From: Trinh Van Dang <dangtv@atvn.com.vn>
  > Sent: 24 March 2020 12:01
  > To: Dhamodharan Krishnamurthy -X (dhakrish - HCL TECHNOLOGIES LIMITED at Cisco) <dhakrish@cisco.com>; 'Nguyen Tien Dung' <dungnt@atvn.com.vn>; thanhnd@atvn.com.vn; cuonglq@atvn.com.vn; 'Nguyen Thanh Nha^n' <nhanngt@atvn.com.vn>; thanhnc@atvn.com.vn; 'Nguyen Khoa Minh Tri' <trinkm@atvn.com.vn>
  > Cc: Tamilselvan Srinivasan -X (tasriniv - HCL TECHNOLOGIES LIMITED at Cisco) <tasriniv@cisco.com>; Chaitra Earappa (chte) <chte@cisco.com>; Balaji Ramani -X (baramani - HCL TECHNOLOGIES LIMITED at Cisco) <baramani@cisco.com>; Vishnu Asok (vasok) <vasok@cisco.com>; Sophia Angelin Caldwell -X (socaldwe - HCL TECHNOLOGIES LIMITED at Cisco) <socaldwe@cisco.com>; Samuel Jebasingh Gnanasampantha Pandian -X (rgnanasa - HCL TECHNOLOGIES LIMITED at Cisco) <rgnanasa@cisco.com>; Nguyen Ngoc Nam <namnn@atvn.com.vn>; Le Thi Buu Tran <tranltb@atvn.com.vn>; Tran Thien Chi <chitt@atvn.com.vn>; Huynh Van Minh <minhhv@atvn.com.vn>; Le Thi Buu Tran <tranltb@atvn.com.vn>; Le Quoc Cuong <cuonglq@atvn.com.vn>; Bui Quang Ngoc <ngocbq@atvn.com.vn>
  >> Subject: Re: B1 Error Notification from Arrive
  >>
  >>  
  >>
  >> Hi Cisco team,
  >>
  >> We did not support B1 BER monitoring from the beginning and none of our products
  >> have this. We just support BER SD/SF alarm which are only defined for Line (B2)
  >> and Path (B3) and these alarms are typically used for APS/UPSR protection.
* **Interrupt restore not work**: We will release an new fpga to fix it 6-apr.

#### Internal

* @a.Nha^n/Dung: Please check and assign issue to member.
* **Some critical/show stopper issues: (it's marking on Zoho)**.

|Issue Prefix |Titile |Assignee - Email|
| ------ | ------ | ------ |
| AC1-I449 | [AF6CCI0071_DV_INT: Interrupt restore just show 1 channels vc1x][AC1-I449] | anhht@atvn.com.vn |
| AC1-I448 | [AF6CCI0071-DV-CEM: Loopback Tu3 was FAILED  in case of Mixing CEM][AC1-I448] | phuongna@atvn.com.vn |
| AC1-I415 | [AF6CCI0071-Mx-DV : PPP: VC3 over BW with cfg = 65,595bytes(92% BW)][AC1-I415] | nhanngt@atvn.com.vn |
| AC1-I406 | [AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406] | thanhnc@atvn.com.vn |
| AC1-I345 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | truongpm@atvn.com.vn |
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

# 23 Mar, 2020
## Critical issue
### 10GMS Cisco AF6CCI0071
1. [<span style="color:red">AF6CCI0071-DV-CEM: BERT engine not sync in case of Mixing CEM</span>][AC1-I448]
  - 18 Mar: Need to Hw check it.
  - 19, 20 Mar: Nothing to update. (Still waiting for Hwer ...)
  - 23 Mar: Ngan/Quang checked it today: "Maybe issue is impacting by tu3 loopback". <span style="color:red">Therefore, need to *SW team* share time to check it</span> .
2. [<span style="color:red">AF6CCI0071-Imsg : Random encap channels Discard All Pkts][AC1-I406]
  - 13 Mar: @a.CThanh was updated SDK as a.LongD cmt but we tried it on-board not successfully. a.LongD will more check it.
  - 16, 17 Mar: Nothing to update.
  - 19 Mar: Issue discard pkt when unbind-bind service was FIXED, but have new issue: unbind-bind service affect other channels. Quang is working with aLong to fix it.
  - 23 Mar: Still waiting for aLong to fix it.
3. [<span style="color:red">AF6CCI0071-Mx-DV : PPP: VC3 over BW with cfg = 65,595bytes(92% BW)][AC1-I415]
  - 23 Mar: This issue  was reported a long time ago. We can't run full BW for Imsg service. Need to Hw share time to check it.
4. <span style="color:red">H.C.Thanh is busy to bring-up new project Raise-Com. Therefore, some issues were paused debugging.</span>
  - 13 - 23 mar: Nothing to update.

## Projects status

### 10GMS Cisco AF6CCI0071

#### Next release

* *10GMS not fast, fix issue*: 6-Apr (old plan: 1-Apr)
* *10GMS Fast, fix issue*: ???, @aNhan, please provide the plan.

#### Issues

##### external

* Cisco is asking a question about "B1 Error Notification from Arrive". Need to a.TAnh share time to feedback it.
* Interrupt restore not work: We will release an new fpga to fix it 6-apr.

##### Internal

* @a.Nha^n/Dung: Please check and assign issue to member.
* *Some critical/show stopper issues: (it's marking on Zoho)*.

| Titile | Assignee - Email|
| ------ | ------ |
| AF6CCI0071-DV-CEM: BERT engine not sync in case of Mixing CEM| nhanngt@atvn.com.vn |
| AF6CCI0071-Mx-DV : PPP: VC3 over BW with cfg = 65,595bytes(92% BW)| nhanngt@atvn.com.vn |
| AF6CCI0071-Imsg : Random encap channels Discard All Pkts | longdt@atvn.com.vn |
| AF6CCI0071_DV_Timing: Have issue when connect with JDSU | nhanngt@atvn.com.vn |
| AF6CCI0071_DV_DCC: Counter MTU is not working | khoams@atvn.com.vn |
| AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G | nhanngt@atvn.com.vn |
| AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out | nganpdk@atvn.com.vn |
| AF6CNC0022_DV_Diag: Ethernet Frame PRBS/Faceplate has not well function | nhanngt@atvn.com.vn |
| AF6CCI0071_DV_Intterupt: Intterupt restore not working | nhanngt@atvn.com.vn |
| AF6CCi0071-Mx-DV : LOPState and LOPSyn is the same | nhanngt@atvn.com.vn |
| AF6CCI0071_DV_PW: PW unbind take long times | longdt@atvn.com.vn |
| AF6CCI0071_DV_ePass: Can't run full BW | nganpdk@atvn.com.vn |
| AF6CCI0071_DV_PDA: Lost block PDA when change many datapath | longdt@atvn.com.vn |
| AF6CCI0071-iMS-Mx-DV-PPP-OverBW: Behavior of overBW not correct | longdt@atvn.com.vn |

### Ciena MRO 20G/10G with CAS

* [The ticket 101][20gmro_ticket_101], Info debug progress:
  * Ciena LAB: need reproduce issue with 250us JB so that dump buffer can capture enough info
  * Arrive: Van Cuong is adding logic to isolate wrong master STS configuration affect linklist storage (current design use this config as storage address) => plan release next debug image within this week
    * 10 Mar: Keep status, nothing to update.
    * 16 Mar: a.VC said "debug image route 2 ngay chua xong, chac add nhieu qua"
    * 17 Mar: *a.VC just sent a new image today. That image has not well function traffic when tried configure path many times (Change configure, not keep). aVC analyzed it and said that HO lost of Block. He will fix it soon*
    * 19 Mar: *a.VC sent a new image today to fix the issue "traffic has not well function when run many times". But, that fpga still failed.* AVC is analyzing more.
    * 20 Mar: Nothing to update.
    * 21-23 Mar: a.VC sent a new image to add debug tool. He checked it and found the root-cause of the issue "re-run traffic many times". He will fix it asap.



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
