# PROJECT STATUS REPORT

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)



# Friday, April 24, 2020

1. STATUS: **<span style="color:GREEN">GREEN**

  * **<span style="color:GREEN">Full QA many projects. But, Tasks are under control**. For more status, you can check links as below:

|Num. | Projects | Status |
| ------ | ------ | ------ |
| 1 | [af6cci0071][af6cci0071] | **<span style="color:YELLOW">YELLOW** |
| 2 | [af6cnc0022][af6cnc0022] | **<span style="color:GREEN">GREEN** |
| 3 | [af6cnc1022][af6cnc1022] | **<span style="color:GREEN">GREEN** |
| 4 | [att_eth_18g][att_eth_18g] | **<span style="color:GREEN">GREEN** |
| 5 | [att_mro_10g][att_mro_10g] | **<span style="color:GREEN">GREEN** |

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Full control to QA the project AF6CCI0071:
    * Control team to full QA the image update restore synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
      - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005621382
    * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon.
  * AF6CNC0022/AF6CNC1022:
    * Confirm the new SDK items with the SDK 2.4.7.b017. Check attached file for more information.
  * ATT ETH 18G:
    * The HW and SW team just updated a latest version (FPGA/SDK) to fix some issues. I helped to check some cases as below:
      - [ATT_ETH_Tester_8a0e0009: EPort counters can't detect DA type packet (Uni, or multi, or broadcast)][O7-43]: The issue was fixed with the new FPGA.
      - [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41]: The issue was fixed with the new FPGA.
      - [ATT_ETH_18G: Support Check Flow Per Port][O7-48]:The issue was fixed with the new FPGA/SDK.
      - [ATT_ETH_18G: Can't run traffic with TPID GLB different Per Flow][O7-52]: The issue was fixed with the new FPGA/SDK.

3. REMAINING WORKLOAD: **BIG**

  * AF6CCI0071:
    * QA the new FPGA update restore based on 5.0 version for next release: 4 May
    * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
    * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.
  * ATT ETH 18G project/ATT MRO 10G:
    * Support Hw/Sw to fix remaining issues.
  * Full control to QA 20G MRO/10G WCAS:
    * Support aVC and team to fix the customer issue ticket 101

4. CRITICAL ISSUES [list keys issues and action plans]

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
| 1 | [AF6CNC1022_DV_SW_PW: Min payload constrain has not been correct][AFL6-I111] | cuonglq@atvn.com.vn | nan | Wait for aQC to update the new strategy.|
| 2 | [AF6CNC1022_DV_SW_PW: LO constrain for JB/payloadsize has not synchronized with each other][AFL6-I109] | cuonglq@atvn.com.vn | nan | Wait for aQC to update the new strategy.|
| 3 | [AF6CNC1022_DV_SW_CEP: SW has displayed the constrain incorrectly][AFL6-I99] | cuonglqs@atvn.com.vn | nan | Wait for aQC to update the new strategy.|

* ATT MRO 10G

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_10G_MRO_DV_SW_PRBS_Device_INIT: PRBS forcing has not been disabled after device init event][MN-216] | khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|
| 2 | [ATT_10G_MRO_DV: STM16/4/1 Can not detect LOS][MN-221] | cuongqc@atvn.com.vn | NONE | The DUT (MRO 20G/10G wCAS) has a require for this case, LOF will detect, not LOS. Therefore, aNhan request set this case is a limitation.|
| 3 | [ATT 10G MRO: Random channel VC12 dectect BIP/REI error when force freqoffs][MN-223] | vuongld@atvn.com.vn | NONE | aNhan said that "Need to Vuong join to check it."|
| 4 | [ATT_10GMRO_DV_HW_SW_SDH: BIP-error rate forcing has not well functioned][MN-230] |khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|
| 5 | [ATT_10G_MRO-DV: Force BIP error VC1x was FAILED][MN-231] |khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|
| 6 | [ATT_10G_MRO_DV_SW_HW_SDH_M1-Byte: M1 function has not worked correctly in all line.][MN232] |khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|


5. MILESTONES

  * AF6CCI0071:
    * Next release: ```Update Restore based on version 5.0 (May 05, 2020), On-track.```
    * Final project (with CEM + PPP): ```NONE```  
  *  20G MRO/10G WCAS:
    * Final project: ```NONE```
  * ATT ETH 18G/ATT MRO 10G: ```None```


# Tuesday, April 21, 2020

1. STATUS: **<span style="color:GREEN">GREEN**

  * **<span style="color:GREEN">Full QA many projects. But, Tasks are under control**. For more status, you can check links as below:

|Num. | Projects | Status |
| ------ | ------ | ------ |
| 1 | [af6cci0071][af6cci0071] | **<span style="color:RED">RED** |
| 2 | [af6cnc0022][af6cnc0022] | **<span style="color:GREEN">GREEN** |
| 3 | [af6cnc1022][af6cnc1022] | **<span style="color:GREEN">GREEN** |
| 4 | [att_eth_18g][att_eth_18g] | **<span style="color:YELLOW">YELLOW** |
| 5 | [att_mro_10g][att_mro_10g] | **<span style="color:GREEN">GREEN** |

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Full control to QA the project AF6CCI0071:
    * Control team to full QA the image fixed many issues, synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
      - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005546149
    * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon. Some issues as below:
      - [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406]: aLongD is analyzing it, don't found the root-cause.
      - [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]: Ngan is analyzing it, don't fount the root-cause.
      - [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345]: Khoa said that ```a Ngan check MPEG for MTU cnt```
    * Support aMinh/Nam to measure time of new way "gen CLI from host": It has an issue with socket buff. aNam is improving it. I will pause this task and back later (if mr.Minh request it).
  * AF6CNC0022/AF6CNC1022:
    * Support Onder (Ciena engineer) via skype.
  * ATT MRO 10G:
    * Work with Hw/Sw to wrap-up this project.

3. REMAINING WORKLOAD: **BIG**

  * AF6CCI0071:
    * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
    * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.
  * ATT ETH 18G project/ATT MRO 10G:
    * Support Hw/Sw to fix remaining issues.
  * Full control to QA 20G MRO/10G WCAS:
    * Support aVC and team to fix the customer issue ticket 101
    * Confirm the new SDK with the the issue [AF6CNC0022_DV_EPass: RF has not well functional on 1000basex][V5-913]

4. CRITICAL ISSUES [list keys issues and action plans]

  - ATT_ETH_18G

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_ETH_18G: Gen traffic 1 shot with random length 64-9600, Pkt always gen with 60 Bytes][O7-54] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 2 | [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 3 | [ATT_ETH_18G: Support Check Flow Per Port][O7-48] | nguyenht@atvn.com.vn | nan | Recheck on the latest version, but raised cafe on err field. Therefore, re-assign to aNguyenHT to recheck it|
| 4 | [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 5 | [ATT_ETH_Tester_8a0e0009: 10G Eth port alarm always UP][O7-40] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|

  - AF6CCI0071

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451] | thanhnc@atvn.com.vn | nan | Fixed it on local SDK, wait for the new official SDK to close.|
| 2 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-17-2020 08:00 | aLongD is analyzing it, don't find a solution to fix it.|
| 3 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | khoams@atvn.com.vn | 04-17-2020 08:00 | It's wrong MRU side also, Khoa just updated RTL code to fix it. Wait for the new FPGA to re-confirm it.|
| 4 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue. Nothing to update.|
| 5 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | Ngan is checking it|
| 6 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it, nothing to update|


  * AF6CNC0022 MRO Ciena:

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [[JIRA] (C6500PTS-101) MRO20G VC4_4c-CEP , Pw is stuck in JB Overrun with high JB level. Traffic is down.][V5-911] | cuongnv@atvn.com.vn | 04-19-2020 08:00 | aVC is trying add some debug tool to analyze.|

  * AF6CNC1022 10G wCAS

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CNC1022_DV_SW_PW: Min payload constrain has not been correct][AFL6-I111] | cuonglq@atvn.com.vn | nan | Wait for aQC to update the new strategy.|
| 2 | [AF6CNC1022_DV_SW_PW: LO constrain for JB/payloadsize has not synchronized with each other][AFL6-I109] | cuonglq@atvn.com.vn | nan | Wait for aQC to update the new strategy.|
| 3 | [AF6CNC1022_DV_SW_CEP: SW has displayed the constrain incorrectly][AFL6-I99] | cuonglqs@atvn.com.vn | nan | Wait for aQC to update the new strategy.|

* ATT MRO 10G

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_10G_MRO_DV_SW_PRBS_Device_INIT: PRBS forcing has not been disabled after device init event][MN-216] | khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|
| 2 | [ATT_10G_MRO_DV: STM16/4/1 Can not detect LOS][MN-221] | cuongqc@atvn.com.vn | NONE | The DUT (MRO 20G/10G wCAS) has a require for this case, LOF will detect, not LOS. Therefore, aNhan request set this case is a limitation.|
| 3 | [ATT 10G MRO: Random channel VC12 dectect BIP/REI error when force freqoffs][MN-223] | vuongld@atvn.com.vn | NONE | aNhan said that "Need to Vuong join to check it."|
| 4 | [ATT_10GMRO_DV_HW_SW_SDH: BIP-error rate forcing has not well functioned][MN-230] |khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|
| 5 | [ATT_10G_MRO-DV: Force BIP error VC1x was FAILED][MN-231] |khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|
| 6 | [ATT_10G_MRO_DV_SW_HW_SDH_M1-Byte: M1 function has not worked correctly in all line.][MN232] |khuongpd@atvn.com.vn | NONE | Wait for SW team to join check it.|


5. MILESTONES

  * AF6CCI0071:
    * Next release: ```Update FEAC (May 05, 2020), On-track.```
    * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```  
  *  20G MRO/10G WCAS:
    * Final project: ```Fixed all issues, Plan: TBD, aQC will provide it.```
  * ATT ETH 18G/ATT MRO 10G: ```None```

# Friday, April 17, 2020

1. STATUS: **<span style="color:GREEN">GREEN**

  * **<span style="color:GREEN">Full QA many projects. But, Tasks are under control**. For more status, you can check links as below:

|Num. | Projects |
| ------ | ------ |
| 1 | [af6cci0071][af6cci0071] |
| 2 | [af6cnc0022][af6cnc0022] |
| 3 | [af6cnc1022][af6cnc1022] |
| 4 | [att_eth_18g][att_eth_18g] |
| 5 | [att_mro_10g][att_mro_10g] |

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Full control to QA the project AF6CCI0071:
    * Control team to full QA the image restore_10 -> Done task.
      - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005430089
    * Control team to full QA the image fixed many issues, synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
      - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005546149
    * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon. Some issues as below:
      - [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406]: aLongD is analyzing it, don't found the root-cause.
      - [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]: Ngan is analyzing it, don't fount the root-cause.
      - [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345]: It's wrong MRU side also, Khoa just updated RTL code to fix it. Wait for the new FPGA to re-confirm it. This issue took time to sync-up meeting with aTu/CThanh/Khoa/Truong.
  * AF6CNC0022/AF6CNC1022:
    * Work a Dinh/aVC to analyze the issue [[JIRA] (C6500PTS-101) MRO20G VC4_4c-CEP , Pw is stuck in JB Overrun with high JB level. Traffic is down.][V5-911].
    * Support Onder (Ciena engineer) via skype.
    * Support HW/SW to chech the issue [RxReorderedPackets always count in case "Force Malformed Packets by configuring tx & expected payload is different"][V5-908].
  * ATT MRO 10G:
    * Work with Hw/Sw to wrap-up this project.

3. REMAINING WORKLOAD: **BIG**

  * AF6CCI0071:
    * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
    * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.
  * ATT ETH 18G project/ATT MRO 10G:
    * Support Hw/Sw to fix remaining issues.
  * Full control to QA 20G MRO/10G WCAS:
    * Support aVC and team to fix the customer issue ticket 101
    * Support a.TCuong fixed the issue [AF6CNC0022_DV_EPass: RF has not well functional on 1000basex][V5-913]

4. CRITICAL ISSUES [list keys issues and action plans]

  - ATT_ETH_18G

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_ETH_18G: Gen traffic 1 shot with random length 64-9600, Pkt always gen with 60 Bytes][O7-54] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 2 | [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 3 | [ATT_ETH_18G: Support Check Flow Per Port][O7-48] | nguyenht@atvn.com.vn | nan | Recheck on the latest version, but raised cafe on err field. Therefore, re-assign to aNguyenHT to recheck it|
| 4 | [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 5 | [ATT_ETH_Tester_8a0e0009: 10G Eth port alarm always UP][O7-40] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|

  - AF6CCI0071

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451] | thanhnc@atvn.com.vn | nan | Fixed it on local SDK, wait for the new official SDK to close.|
| 2 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-17-2020 08:00 | aLongD is analyzing it, don't find a solution to fix it.|
| 3 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | khoams@atvn.com.vn | 04-17-2020 08:00 | It's wrong MRU side also, Khoa just updated RTL code to fix it. Wait for the new FPGA to re-confirm it.|
| 4 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue. Nothing to update.|
| 5 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | Ngan is checking it|
| 6 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it, nothing to update|


  * AF6CNC0022 MRO Ciena:

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [[JIRA] (C6500PTS-101) MRO20G VC4_4c-CEP , Pw is stuck in JB Overrun with high JB level. Traffic is down.][V5-911] | cuongnv@atvn.com.vn | 04-19-2020 08:00 | aVC is trying add some debug tool to analyze.|

  * AF6CNC1022 10G wCAS

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CNC1022_DV_SW_PW: Min payload constrain has not been correct][AFL6-I111] | cuonglq@atvn.com.vn | nan | Wait for aQC to update the new strategy.|
| 2 | [AF6CNC1022_DV_SW_PW: LO constrain for JB/payloadsize has not synchronized with each other][AFL6-I109] | cuonglq@atvn.com.vn | nan | Wait for aQC to update the new strategy.|
| 3 | [AF6CNC1022_DV_SW_CEP: SW has displayed the constrain incorrectly][AFL6-I99] | cuonglqs@atvn.com.vn | nan | Wait for aQC to update the new strategy.|

* ATT MRO 10G

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_ETH_18G: Gen traffic 1 shot with random length 64-9600, Pkt always gen with 60 Bytes][O7-54] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 2 | [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 3 | [ATT_ETH_18G: Support Check Flow Per Port][O7-48] | nguyenht@atvn.com.vn | nan | Recheck on the latest version, but raised cafe on err field. Therefore, re-assign to aNguyenHT to recheck it|
| 4 | [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 5 | [ATT_ETH_Tester_8a0e0009: 10G Eth port alarm always UP][O7-40] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|


5. MILESTONES

  * AF6CCI0071:
    * Next release: ```Update FEAC (May 05, 2020), On-track.```
    * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```  
  *  20G MRO/10G WCAS:
    * Final project: ```Fixed all issues, Plan: TBD, aQC will provide it.```
  * ATT ETH 18G/ATT MRO 10G:
    * Final project: ```Fixed all issues, Plan: TBD, aNhan will provide it.```


# Tuesday, April 14, 2020

1. STATUS: **<span style="color:GREEN">GREEN**

  * **<span style="color:GREEN">Full QA many projects. But, Tasks are under control**. For more status, you can check links as below:

|Num. | Projects |
| ------ | ------ |
| 1 | [af6cci0071][af6cci0071] |
| 2 | [af6cnc0022][af6cnc0022] |
| 3 | [af6cnc1022][af6cnc1022] |
| 4 | [att_eth_18g][att_eth_18g] |

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Support and check some issues with ATT ETH 18G project.
    * Re-check the issue [ATT_ETH_18G: Gen payload PRBS11 but DUT detect all0s][O7-44] with the new SDK: ```Closed this issue.```
    * Re-check the issue [ATT_ETH_18G: Support Check Flow Per Port][O7-48] with the new SDK: ```Recheck on the latest version, but raised cafe on err field. Therefore, re-assign to aNguyenHT to recheck it```.
    * Re-check the issue [ATT_ETH_Tester_8a0e0009: New request to support FCS ERR PKT][O7-42] with the new SDK: ```Closed this issue.```
  * Full control to QA the project AF6CCI0071:
    * As a.Nhan requested, our team (DV) shared a day to up-to-date the test-plan file status.
      - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005539305
    * Control team to full QA the image restore_10 -> Hope done it end of this week:
      - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005430089
    * Control team to full QA the image fixed many issues, synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
      - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005546149
    * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon.
  * AF6CNC0022:
    * I helped aVC to check some debug images:
      - AF6CNC0022_OCNMRO_20G_8.1_80.45_Apr_11_2020_07h35m.bin: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000000038143/403027000004562009/403027000005546379
      - AF6CNC0022_OCNMRO_20G_8.1_80.45_Apr_12_2020_05h14m.bin: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000000038143/403027000004562009/403027000005546397

3. REMAINING WORKLOAD: **BIG**

  * AF6CCI0071:
    * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
    * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.
  * ATT ETH 18G project.
    * Support Hw/Sw to fix remaining issues.
    * Full control to QA 20G MRO/10G WCAS:
      * Support aVC and team to fix the customer issue ticket 101
      * Support a.TCuong fixed the issue [AF6CNC0022_DV_EPass: RF has not well functional on 1000basex][V5-913]

4. CRITICAL ISSUES [list keys issues and action plans]

  - ATT_ETH_18G

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_ETH_18G: Gen traffic 1 shot with random length 64-9600, Pkt always gen with 60 Bytes][O7-54] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 2 | [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 3 | [ATT_ETH_18G: Support Check Flow Per Port][O7-48] | nguyenht@atvn.com.vn | nan | Recheck on the latest version, but raised cafe on err field. Therefore, re-assign to aNguyenHT to recheck it|
| 4 | [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 5 | [ATT_ETH_Tester_8a0e0009: 10G Eth port alarm always UP][O7-40] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|

  - AF6CCI0071

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451] | nhanngt@atvn.com.vn | nan | Fixed it on local SDK, wait for the new official SDK to close.|
| 2 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-17-2020 08:00 | Don't find a solution to fix it.|
| 3 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | khoams@atvn.com.vn | 04-17-2020 08:00 | Khoa is busy for other project. Wait for him to check this issue.|
| 4 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue.|
| 5 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | Ngan is checking it|
| 6 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it|


  * AF6CNC0022 MRO Ciena:

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [[JIRA] (C6500PTS-101) MRO20G VC4_4c-CEP , Pw is stuck in JB Overrun with high JB level. Traffic is down.][V5-911] | cuongnv@atvn.com.vn | 04-19-2020 08:00 | aVC is trying add some debug tool to analyze.|

  * AF6CNC1022 10G wCAS

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CNC1022_DV_SW_PW: Min payload constrain has not been correct][AFL6-I111] | dinhnl@atvn.com.vn | nan | Wait for aDinh to check it|
| 2 | [AF6CNC1022_DV_SW_PW: LO constrain for JB/payloadsize has not synchronized with each other][AFL6-I109] | dinhnl@atvn.com.vn | nan | Wait for aDinh to check it|
| 3 | [AF6CNC1022_DV_SW_CEP: SW has displayed the constrain incorrectly][AFL6-I99] | bangnv@atvn.com.vn | nan | Bang will try it on the latest version|


5. MILESTONES

  * AF6CCI0071:
    * Next release: ```Update FEAC (May 05, 2020), On-track.```
    * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```  
  *  20G MRO/10G WCAS:
    * Final project: ```Fixed all issues, Plan: TBD, aQC will provide it.```
  * ATT ETH 18G:
    * Final project: ```Fixed all issues, Plan: TBD, aNhan will provide it.```


# Friday, April 10, 2020

1. STATUS: **<span style="color:GREEN">GREEN**

  * **<span style="color:GREEN">Full QA many projects. But, Tasks are under control**. For more status, you can check links as below:

|Num. | Projects |
| ------ | ------ |
| 1 | [af6cci0071][af6cci0071] |
| 2 | [af6cnc0022][af6cnc0022] |
| 3 | [af6cnc1022][af6cnc1022] |
| 4 | [att_eth_18g][att_eth_18g] |

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * <span style="color:GREEN">Finished define test-cases on CEM_IMSG App.
  * Support 10GMS Ciena for Ethernet passthrough testing.
  * Full control to QA 10GMS Cisco AF6CCI0071:
    * **<span style="color:GREEN">We just fixed the issue "interrupt restore" and official release to Cisco Apr 6, 2020. DV team and others teams were hard work to QA that version last time.**
    * Take lots of time to check/analyze the customer issue ```ticket 9522```. This issue was fixed on the sdk 4.4.10. Therefore, wait for Cisco to confirm it on the latest version.
    * Support Hw/SW to check the remaining issues
  * Full control to QA 20G MRO/10G WCAS:
    * Support aVC and team to fix the customer issue ticket 101
    * Support a.TCuong fixed the issue [AF6CNC0022_DV_EPass: RF has not well functional on 1000basex][V5-913]
  * SUpport and check some issues with ATT ETH 18G project.


3. REMAINING WORKLOAD: **BIG**

  * 10GMS Cisco af6cci0071:
    * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
    * Support Hw/SW to check the remaining issues  
  * Full control to QA 20G MRO/10G WCAS:
    * Support aVC and team to fix the customer issue ticket 101
    * Support a.TCuong fixed the issue [AF6CNC0022_DV_EPass: RF has not well functional on 1000basex][V5-913]
  * ATT ETH 18G: Support Hw/Sw to fix remaining issues.

4. CRITICAL ISSUES [list keys issues and action plans]

  * 10GMS Cisco af6cci0071

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451] | nhanngt@atvn.com.vn | nan | aLongD/Thanh are finding a solution to fix this issue and the issue AC1-I406 also.|
| 2 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | thanhnc@atvn.com.vn | 04-17-2020 08:00 | aLongD/Thanh are finding a solution to fix this issue and the issue AC1-I406 also.|
| 3 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | khoams@atvn.com.vn | 04-17-2020 08:00 | Khoa is busy for other project. Wait for him to check this issue.|
| 4 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr"|
| 5 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | Quang will support Ngan a detail scripts to check this issue next week, he busy to support check some customers in this week|
| 6 | [AF6CCi0071-Mx-DV : LOPState and LOPSyn is the same][AC1-I253] | nhanngt@atvn.com.vn | 04-18-2019 18:00 | Wait for HWer to check it|
| 7 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it|
| 8 | [AF6CCI0071_DV_PDA: Lost block PDA when change many datapath][AC1-I172] | longdt@atvn.com.vn | 03-22-2019 18:00 | Wait for HWer to check it|
| 9 | [AF6CCI0071-iMS-Mx-DV-PPP-OverBW: Behavior of overBW not correct][AC1-I136] | quangnm@atvn.com.vn | 03-06-2019 17:00 | Quang will try it with the latest version|

  * AF6CNC0022 MRO Ciena:

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [[JIRA] (C6500PTS-101) MRO20G VC4_4c-CEP , Pw is stuck in JB Overrun with high JB level. Traffic is down.][V5-911] | cuongnv@atvn.com.vn | 04-19-2020 08:00 | aVC is trying add some debug tool to analyze.|

  * AF6CNC1022 10G wCAS

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CNC1022_DV_SW_PW: Min payload constrain has not been correct][AFL6-I111] | dinhnl@atvn.com.vn | nan | Wait for aDinh to check it|
| 2 | [AF6CNC1022_DV_SW_PW: LO constrain for JB/payloadsize has not synchronized with each other][AFL6-I109] | dinhnl@atvn.com.vn | nan | Wait for aDinh to check it|
| 3 | [AF6CNC1022_DV_SW_CEP: SW has displayed the constrain incorrectly][AFL6-I99] | bangnv@atvn.com.vn | nan | Bang will try it on the latest version|

  * ATT_ETH_18G

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_ETH_18G: Gen traffic 1 shot with random length 64-9600, Pkt always gen with 60 Bytes][O7-54] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 2 | [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 3 | [ATT_ETH_18G: Support Check Flow Per Port][O7-48] | dangtv@atvn.com.vn | nan | I will try it on next week|
| 4 | [ATT_ETH_Tester_8a0e0009: New request to support FCS ERR PKT][O7-42] | dangtv@atvn.com.vn | nan | I will try it on next week|
| 5 | [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 6 | [ATT_ETH_Tester_8a0e0009: 10G Eth port alarm always UP][O7-40] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|


5. MILESTONES

  * AF6CCI0071:
    * Next release: ```Update FEAC (May 05, 2020), On-track.```
    * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```  
  *  20G MRO/10G WCAS:
    * Final project: ```Fixed all issues, Plan: TBD, aQC will provide it.```
  * ATT ETH 18G:
    * Final project: ```Fixed all issues, Plan: TBD, aNhan will provide it.```


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
