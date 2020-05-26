# PROJECT_ID: DV department
# PROJECT STATUS REPORT: WEEK#19/2020

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)

1. STATUS: **<span style="color:GREEN">GREEN**

  * Except 10GMS Cisco project (FEAC, FPGA not ready; Hw issues stuck, not have member to debug), otherwises Ok. For more status, you can check as below:

|Num. | Projects | Status |
| ------ | ------ | ------ |
| 1 | [af6cci0071][af6cci0071] | **<span style="color:RED">RED** |
| 2 | [af6cnc0022][af6cnc0022] | **<span style="color:GREEN">GREEN** |
| 3 | [af6cnc1022][af6cnc1022] | **<span style="color:GREEN">GREEN** |
| 4 | [att_eth_18g][att_eth_18g] | **<span style="color:GREEN">GREEN** |
| 5 | [att_mro_10g][att_mro_10g] | **<span style="color:GREEN">GREEN** |

2. KEY ACCOMPLISHMENTS [Compared to previous report]:

  * Support aMinh/aNam to check new auto-testupdate wqith cli_session.
  * Full control to QA the project AF6CCI0071:
    * The FPGA support FEAC (18 May) is not ready now. Therefore, We still QA the image for update interrupt restore:
      - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005621382
    * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon.

3. ACTION PLAN FOR NEXT WEEK

  * AF6CCI0071:
    * QA the new FPGA update `FEAC` for next release: ```18 May```
  * ATT ETH 18G project/ATT MRO 10G (If have):
    * Support Hw/Sw to fix remaining issues.
  * Full control to QA 20G MRO/10G WCAS (If have):
    * Support aVC and team to fix the customer issue ticket 101
  * 10GMS Ciena: Support to check Ethernet pass-through issues (If have).
  * DV: Finish guideline file as a.Minh request.

4. REMAINING WORKLOAD: ```BIG```

  * AF6CCI0071:
    * QA the new FPGA update `FEAC` for next release: ```18 May```
    * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.
  * ATT ETH 18G project/ATT MRO 10G:
    * Support Hw/Sw to fix remaining issues.
  * Full control to QA 20G MRO/10G WCAS:
    * Support aVC and team to fix the customer issue ticket 101
  * 10GMS Ciena: Support to check Ethernet pass-through issues (If have).
  * DV: Finish guideline file as a.Minh request.

5. CRITICAL ISSUES [list keys issues and action plans]


  - ATT_ETH_18G

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_ETH_18G: Gen traffic 1 shot with random length 64-9600, Pkt always gen with 60 Bytes][O7-54] | khuongpd@atvn.com.vn | nan | wait for Swer to check it|
| 2 | [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 3 | [ATT_ETH_Tester_8a0e0009: 10G Eth port alarm always UP][O7-40] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|

  - AF6CCI0071

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-30-2020 08:00 | aLongD is analyzing it, don't find a solution to fix it.|
| 2 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | nganpdk@atvn.com.vn | 04-17-2020 08:00 | MRU Ok, Stuck Ngan at MTU|
| 3 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue. Nothing to update.|
| 4 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | aNhan said that, found a same root-casue on 10GMS Ciena, wait for apply form that project to this project|
| 5 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it, nothing to update|



  * AF6CNC0022 MRO Ciena:

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [[JIRA] (C6500PTS-101) MRO20G VC4_4c-CEP , Pw is stuck in JB Overrun with high JB level. Traffic is down.][V5-911] | cuongnv@atvn.com.vn | 04-19-2020 08:00 | aVC is trying add some debug tool to analyze.|

  * AF6CNC1022 10G wCAS

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CNC1022_DV_SW_PW: LO constrain for JB/payloadsize has not synchronized with each other][AFL6-I109] | cuonglq@atvn.com.vn | nan | Wait for aQC to update the new strategy.|
| 2 | [AF6CNC1022_DV_SW_CEP: SW has displayed the constrain incorrectly][AFL6-I99] | cuonglqs@atvn.com.vn | nan | Wait for aQC to update the new strategy.|

* ATT MRO 10G

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_10G_MRO_DV_SW_PRBS_Device_INIT: PRBS forcing has not been disabled after device init event][MN-216] | khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|
| 2 | [ATT 10G MRO: Random channel VC12 dectect BIP/REI error when force freqoffs][MN-223] | vuongld@atvn.com.vn | NONE | aNhan said that "Need to Vuong join to check it."|
| 3 | [ATT_10GMRO_DV_HW_SW_SDH: BIP-error rate forcing has not well functioned][MN-230] |khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|
| 4 | [ATT_10G_MRO-DV: Force BIP error VC1x was FAILED][MN-231] |khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|
| 5 | [ATT_10G_MRO_DV_SW_HW_SDH_M1-Byte: M1 function has not worked correctly in all line.][MN-232] |khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|

6. MILESTONES/TASK BREAKDOWN:

  * AF6CCI0071:
    * Update ```FEAC```: May 18, 2020; The FPGA is not ready now -> That's impacting to next release.
    * Wrap-up the phase "CEM, Imsg/PPP": Plan: ```None```; The FPGA is not ready now (PDA/MPEG hangout, but RTL don't time to check it).

  *  20G MRO/10G WCAS:
    * Final project: ```NONE```
  * ATT ETH 18G/ATT MRO 10G: `NONE`

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


  [af6cci0071]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003100013/403027000003100103>
  [af6cnc0022]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000000038143/403027000001958175/403027000001958181>
  [af6cnc1022]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000002463129/403027000002467545/403027000002467671>
  [att_eth_18g]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000002130382/403027000002135009/403027000005519381>
  [att_mro_10g]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000001176113/403027000002065310/403027000002065316>  

  [AC1-I451]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005457481>
  [AC1-I406]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000005000092>
  [AC1-I400]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004959321>
  [AC1-I371]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004783041>
  [AC1-I365]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004679200>
  [AC1-I364]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004722049>
  [AC1-I345]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004614259>
  [AC1-I344]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004611065>
  [AC1-I343]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004611044>
  [AC1-I328]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004546009>
  [AC1-I324]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004542007>
  [AC1-I296]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004357407>
  [AC1-I253]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004168021>
  [AC1-I245]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004148065>
  [AC1-I228]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004104093>
  [AC1-I223]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004095246>
  [AC1-I211]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004066219>
  [AC1-I209]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004066141>
  [AC1-I193]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004046420>
  [AC1-I192]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004046401>
  [AC1-I186]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004048184>
  [AC1-I178]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004035577>
  [AC1-I172]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000004020719>
  [AC1-I147]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000003965182>
  [AC1-I136]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000003933388>
  [AC1-I65]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000003684436>
  [AC1-I45]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000003095123/403027000003660083>

  [V5-913]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000000038143/403027000005479169>
  [V5-911]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000000038143/403027000005218144>
  [V5-908]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000000038143/403027000005167385>

  [AFL6-I114]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004693415>
  [AFL6-I111]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004598553>
  [AFL6-I110]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004598325>
  [AFL6-I109]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004592024>
  [AFL6-I105]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004582183>
  [AFL6-I103]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004576223>
  [AFL6-I100]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004463088>
  [AFL6-I99]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004463017>
  [AFL6-I94]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004174627>
  [AFL6-I93]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002463129/403027000004174602>  

  [O7-54]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000005415138>
  [O7-53]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000005402377>
  [O7-52]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000005116047>
  [O7-48]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004970083>
  [O7-44]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004935179>
  [O7-43]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004917118>
  [O7-42]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004890053>
  [O7-41]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004890030>
  [O7-40]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004890007>

  [MN-216]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000001176113/403027000004509167>
  [MN-221]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000001176113/403027000004715125>
  [MN-223]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000001176113/403027000004842032>
  [MN-230]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000001176113/403027000005189053>
  [MN-231]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000001176113/403027000005247007>
  [MN-232]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000001176113/403027000005613322>  
