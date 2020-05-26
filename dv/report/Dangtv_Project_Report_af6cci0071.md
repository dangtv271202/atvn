# PROJECT STATUS REPORT

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)


# Tuesday, April 24, 2020

1. STATUS: **<span style="color:YELLOW">YELLOW**

  * **<span style="color:RED">Warning: Many issues don't progress (PDA/MPEG). It's impacting to wrap-up phase-1 of this project.**
  * We divided it for 2 phases:
    - Phase 1: Support CEM + Imsg/PPP_only. This phase is in wrap-up phase, with:
      + CEM:
        ++ Update Restore based on version 5.0 (```May 4, 2020```): ```The image is QA, on-track```
        ++ Update FEAC (```May 11, 2020```): ```Wait for apply from 3GMS first, DV is waiting for a new image to confirm it.```
      + Imsg: Fixed all remain issues. Currently, It's stuck a PDA/MPEG issues.
    - Phase 2: Final, CEM + Ether pass + Imsg (PPP/MLPPP/FR/MFR) + LCAS/VCAS. Currently, it's not ready on-board

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Control team to full QA the image update restore synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
    - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005621382
  * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon.

3. REMAINING WORKLOAD: **BIG**

  * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
  * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.

4. CRITICAL ISSUES [list keys issues and action plans]

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-30-2020 08:00 | aLongD is analyzing it, don't find a solution to fix it.|
| 2 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | nganpdk@atvn.com.vn | 04-17-2020 08:00 | MRU Ok, Stuck Ngan at MTU|
| 3 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue. Nothing to update.|
| 4 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | aNhan said that, found a same root-casue on 10GMS Ciena, wait for apply form that project to this project|
| 5 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it, nothing to update|

5. MILESTONES
  * Next release:
    - Update Restore based on version 5.0: ```(May 11, 2020), On-track.```
    - Update FEAC: ```(May 11, 2020), The FPGA is not ready now, Wait for apply on 3GMS project first.```
  * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```
  * Full image: ```FPGA/SDK are not ready now.```


# Tuesday, April 21, 2020

1. STATUS: **<span style="color:RED">RED**

  * **<span style="color:RED">Many issues don't progress. It's impacting to wrap-up phase-1 of this project. Therefore, change status to RED.**
  * We divided it for 2 phases:
    - Phase 1: Support CEM + Imsg/PPP_only. This phase is in wrap-up phase, with:
      + CEM: Update FEAC. Plan: Release it May 5, 2020. Status: Wait for apply from 3GMS first, DV is waiting for a new image to confirm it.
      + Imsg: Fixed all remain issues. Currently, It's stuck a PDA/MPEG issue. aLong/Ngan are analyzing it As aNhan requested, hope we have a final image about April 30, 2020.
    - Phase 2: Final, CEM + Ether pass + Imsg (PPP/MLPPP/FR/MFR) + LCAS/VCAS. Currently, it's not ready on-board

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Control team to full QA the image fixed many issues, synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
    - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005546149
  * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon. Some issues as below:
    - [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406]: aLongD is analyzing it, don't found the root-cause.
    - [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]: Ngan is analyzing it, don't fount the root-cause.
    - [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345]: Khoa said that ```a Ngan check MPEG for MTU cnt```
  * Support aMinh/Nam to measure time of new way "gen CLI from host": It has an issue with socket buff. aNam is improving it. I will pause this task and back later (if mr.Minh request it).

3. REMAINING WORKLOAD: **BIG**

  * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
  * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.

4. CRITICAL ISSUES [list keys issues and action plans]

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451] | thanhnc@atvn.com.vn | nan | Fixed it on local SDK, wait for the new official SDK to close.|
| 2 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-17-2020 08:00 | aLongD is analyzing it, don't find a solution to fix it.|
| 3 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | khoams@atvn.com.vn | 04-17-2020 08:00 | It's wrong MRU side also, Khoa just updated RTL code to fix it. Wait for the new FPGA to re-confirm it.|
| 4 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue. Nothing to update.|
| 5 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | Ngan is checking it|
| 6 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it, nothing to update|

5. MILESTONES

  * Next release: ```Update FEAC (May 05, 2020), On-track.```
  * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```
  * Full image: ```FPGA/SDK are not ready now.```


# Tuesday, April 21, 2020

1. STATUS: **<span style="color:RED">RED**

  * **<span style="color:RED">Many issues don't progress. It's impacting to wrap-up phase-1 of this project. Therefore, change status to RED.**
  * We divided it for 2 phases:
    - Phase 1: Support CEM + Imsg/PPP_only. This phase is in wrap-up phase, with:
      + CEM: Update FEAC. Plan: Release it May 5, 2020. Status: Wait for apply from 3GMS first, DV is waiting for a new image to confirm it.
      + Imsg: Fixed all remain issues. Currently, It's stuck a PDA/MPEG issue. aLong/Ngan are analyzing it As aNhan requested, hope we have a final image about April 30, 2020.
    - Phase 2: Final, CEM + Ether pass + Imsg (PPP/MLPPP/FR/MFR) + LCAS/VCAS. Currently, it's not ready on-board

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Control team to full QA the image fixed many issues, synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
    - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005546149
  * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon. Some issues as below:
    - [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406]: aLongD is analyzing it, don't found the root-cause.
    - [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]: Ngan is analyzing it, don't fount the root-cause.
    - [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345]: Khoa said that ```a Ngan check MPEG for MTU cnt```
  * Support aMinh/Nam to measure time of new way "gen CLI from host": It has an issue with socket buff. aNam is improving it. I will pause this task and back later (if mr.Minh request it).

3. REMAINING WORKLOAD: **BIG**

  * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
  * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.

4. CRITICAL ISSUES [list keys issues and action plans]

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-30-2020 08:00 | aLongD is analyzing it, don't find a solution to fix it.|
| 2 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | nganpdk@atvn.com.vn | 04-17-2020 08:00 | It's wrong MRU side also, Khoa just updated RTL code to fix it. Wait for the new FPGA to re-confirm it.|
| 3 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue. Nothing to update.|
| 4 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | aNhan said that, found a same root-casue on 10GMS Ciena, wait for apply form that project to this project|
| 5 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it, nothing to update|

5. MILESTONES
  * Next release:
    - Update Restore based on version 5.0: ```(May 11, 2020), On-track.```
    - Update FEAC: ```(May 11, 2020), The FPGA is not ready now, Wait for apply on 3GMS project first.```
  * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```
  * Full image: ```FPGA/SDK are not ready now.```


# Tuesday, April 21, 2020

1. STATUS: **<span style="color:RED">RED**

  * **<span style="color:RED">Many issues don't progress. It's impacting to wrap-up phase-1 of this project. Therefore, change status to RED.**
  * We divided it for 2 phases:
    - Phase 1: Support CEM + Imsg/PPP_only. This phase is in wrap-up phase, with:
      + CEM: Update FEAC. Plan: Release it May 5, 2020. Status: Wait for apply from 3GMS first, DV is waiting for a new image to confirm it.
      + Imsg: Fixed all remain issues. Currently, It's stuck a PDA/MPEG issue. aLong/Ngan are analyzing it As aNhan requested, hope we have a final image about April 30, 2020.
    - Phase 2: Final, CEM + Ether pass + Imsg (PPP/MLPPP/FR/MFR) + LCAS/VCAS. Currently, it's not ready on-board

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Control team to full QA the image fixed many issues, synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
    - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005546149
  * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon. Some issues as below:
    - [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406]: aLongD is analyzing it, don't found the root-cause.
    - [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]: Ngan is analyzing it, don't fount the root-cause.
    - [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345]: Khoa said that ```a Ngan check MPEG for MTU cnt```
  * Support aMinh/Nam to measure time of new way "gen CLI from host": It has an issue with socket buff. aNam is improving it. I will pause this task and back later (if mr.Minh request it).

3. REMAINING WORKLOAD: **BIG**

  * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
  * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.

4. CRITICAL ISSUES [list keys issues and action plans]

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451] | thanhnc@atvn.com.vn | nan | Fixed it on local SDK, wait for the new official SDK to close.|
| 2 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-17-2020 08:00 | aLongD is analyzing it, don't find a solution to fix it.|
| 3 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | khoams@atvn.com.vn | 04-17-2020 08:00 | It's wrong MRU side also, Khoa just updated RTL code to fix it. Wait for the new FPGA to re-confirm it.|
| 4 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue. Nothing to update.|
| 5 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | Ngan is checking it|
| 6 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it, nothing to update|

5. MILESTONES

  * Next release: ```Update FEAC (May 05, 2020), On-track.```
  * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```
  * Full image: ```FPGA/SDK are not ready now.```

# Friday, April 17, 2020

1. STATUS: **<span style="color:YELLOW">YELLOW**

  * **<span style="color:GREEN">HW/SW and DV are hard working last time. Many issues were fixed.**
  * We divided it for 2 phases:
    - Phase 1: Support CEM + Imsg/PPP_only. This phase is in wrap-up phase, with:
      + CEM: Update FEAC. Plan: Release it May 5, 2020. Status: Wait for apply from 3GMS first, DV is waiting for a new image to confirm it.
      + Imsg: Fixed all remain issues. Currently, It's stuck a PDA/MPEG issue. aLong/Ngan are analyzing it As aNhan requested, hope we have a final image about April 30, 2020.
    - Phase 2: Final, CEM + Ether pass + Imsg (PPP/MLPPP/FR/MFR) + LCAS/VCAS. Currently, it's not ready on-board

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Control team to full QA the image restore_10 -> Done task.
    - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005430089
  * Control team to full QA the image fixed many issues, synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
    - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005546149
  * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon. Some issues as below:
    - [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406]: aLongD is analyzing it, don't found the root-cause.
    - [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324]: Ngan is analyzing it, don't fount the root-cause.
    - [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345]: It's wrong MRU side also, Khoa just updated RTL code to fix it. Wait for the new FPGA to re-confirm it. This issue took time to sync-up meeting with aTu/CThanh/Khoa/Truong.

3. REMAINING WORKLOAD: **BIG**

  * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
  * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.

4. CRITICAL ISSUES [list keys issues and action plans]

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451] | thanhnc@atvn.com.vn | nan | Fixed it on local SDK, wait for the new official SDK to close.|
| 2 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-17-2020 08:00 | aLongD is analyzing it, don't find a solution to fix it.|
| 3 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | khoams@atvn.com.vn | 04-17-2020 08:00 | It's wrong MRU side also, Khoa just updated RTL code to fix it. Wait for the new FPGA to re-confirm it.|
| 4 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue. Nothing to update.|
| 5 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | Ngan is checking it|
| 6 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it, nothing to update|

5. MILESTONES

  * Next release: ```Update FEAC (May 05, 2020), On-track.```
  * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```
  * Full image: ```FPGA/SDK are not ready now.```


# Tuesday, April 14, 2020

1. STATUS: **<span style="color:YELLOW">YELLOW**

  * **<span style="color:GREEN">HW/SW and DV are hard working last time. Many issues were fixed.**
  * In this phase, we will create a plan to wrap-up this project with ```"CEM + Imsg/Ppp"``` service. Therefore, all issues should close (Currently, the total issue is 24).

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * As a.Nhan requested, our team (DV) shared a day to up-to-date the test-plan file status.
    - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005539305
  * Control team to full QA the image restore_10 -> Hope done it end of this week:
    - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005430089
  * Control team to full QA the image fixed many issues, synt it based on fast_search image. Plan: release it 5 May 2020 (Note that it's not update FEAC yet)
    - Zoho link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000003770191/403027000005546149
  * Support Hw/SW fix remaining issues. Hope wrap-up this project with ```CEM/Imsg/PPP``` soon.

3. REMAINING WORKLOAD: **BIG**

  * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
  * Support Hw/SW to check the remaining issues. Hope to wrap-up the phase "CEM, Imsg/PPP" soon.

4. CRITICAL ISSUES [list keys issues and action plans]

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [AF6CCi0071-DV-Imsg: Device init 1 time when change path make hang out traffic][AC1-I451] | nhanngt@atvn.com.vn | nan | Fixed it on local SDK, wait for the new official SDK to close.|
| 2 | [AF6CCI0071-Imsg : PDA: Random channels Discard All Pkts][AC1-I406] | longdt@atvn.com.vn | 04-17-2020 08:00 | Don't find a solution to fix it.|
| 3 | [AF6CCI0071_DV_DCC: Counter MTU is not working][AC1-I345] | khoams@atvn.com.vn | 04-17-2020 08:00 | Khoa is busy for other project. Wait for him to check this issue.|
| 4 | [AF6CCI0071-Mx-DV : PPP: VC4_16C over BW with cfg = 2,45G][AC1-I328] | nhanngt@atvn.com.vn | 04-13-2020 08:00 | aNha^n said: "PPP set low priority, Come back: 13Apr". It's overdue.|
| 5 | [AF6CCi0071-Mx-DV : PPP: normal path - MPEG hang out][AC1-I324] | nganpdk@atvn.com.vn | nan | Ngan is checking it|
| 6 | [AF6CCI0071_DV_PW: PW unbind take long times][AC1-I186] | longdt@atvn.com.vn | nan | Wait for HWer to check it|

5. MILESTONES

  * Next release: ```Update FEAC (May 05, 2020), On-track.```
  * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```

# Friday, April 10, 2020

1. STATUS: **<span style="color:YELLOW">YELLOW**

  * **<span style="color:GREEN">HW/SW and DV are hard working last time. Many issues were fixed.**
  * **<span style="color:GREEN">We just fixed the issue "interrupt restore" and official release to Cisco Apr 6, 2020.**
  * In this phase, we will create a plan to wrap-up this project with "CEM + Imsg/Ppp" service. Therefore, all issues should close (Currently, the total issue is 27).

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * **<span style="color:GREEN">We just fixed the issue "interrupt restore" and official release to Cisco Apr 6, 2020. DV team and others teams were hard work to QA that version last time.**
  * Take lots of time to check/analyze the customer issue ```ticket 9522```. This issue was fixed on the sdk 4.4.10. Therefore, wait for Cisco to confirm it on the latest version.
  * Support Hw/SW to check the remaining issues

3. REMAINING WORKLOAD: **BIG**

  * Wait for update FEAC done on 3GMS project. Then, apply it 10GMS to QA new FPGA for next release.
  * Support Hw/SW to check the remaining issues

4. CRITICAL ISSUES [list keys issues and action plans]

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

5. MILESTONES

  * Next release: ```Update FEAC (May 05, 2020), On-track.```
  * Final project (with CEM + PPP): ```Wait for a.Nhan provide it```


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

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
