# PROJECT STATUS REPORT

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)


# Friday, April 24, 2020


1. STATUS: **<span style="color:GREEN">GREEN**

  * **<span style="color:GREEN">This project is in phase wrap-up**. We are working to clear all issues.

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * The HW and SW team just updated a latest version (FPGA/SDK) to fix some issues. I helped to check some cases as below:
    - [ATT_ETH_Tester_8a0e0009: EPort counters can't detect DA type packet (Uni, or multi, or broadcast)][O7-43]: The issue was fixed with the new FPGA.
    - [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41]: The issue was fixed with the new FPGA.
    - [ATT_ETH_18G: Support Check Flow Per Port][O7-48]:The issue was fixed with the new FPGA/SDK.
    - [ATT_ETH_18G: Can't run traffic with TPID GLB different Per Flow][O7-52]: The issue was fixed with the new FPGA/SDK.

3. REMAINING WORKLOAD: **MEDIUM**

  * Support Hw/Sw to fix remaining issues.

4. CRITICAL ISSUES [list keys issues and action plans]

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_ETH_18G: Gen traffic 1 shot with random length 64-9600, Pkt always gen with 60 Bytes][O7-54] | khuongpd@atvn.com.vn | nan | wait for Swer to check it|
| 2 | [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 3 | [ATT_ETH_Tester_8a0e0009: 10G Eth port alarm always UP][O7-40] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|


5. MILESTONES

  * Final project: ```Fixed all issues, Plan: TBD, aNhan will provide it.```


# Tuesday, April 21, 2020

Nothing to update.

# Friday, April 17, 2020

Nothing to update.

# Tuesday, April 14, 2020

1. STATUS: **<span style="color:YELLOW">YELLOW**

  * **<span style="color:GREEN">This project is in phase wrap-up**. We are working to clear all issues.

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * Re-check the issue [ATT_ETH_18G: Gen payload PRBS11 but DUT detect all0s][O7-44] with the new SDK: ```Closed this issue.```
  * Re-check the issue [ATT_ETH_18G: Support Check Flow Per Port][O7-48] with the new SDK: ```Recheck on the latest version, but raised cafe on err field. Therefore, re-assign to aNguyenHT to recheck it```.
  * Re-check the issue [ATT_ETH_Tester_8a0e0009: New request to support FCS ERR PKT][O7-42] with the new SDK: ```Closed this issue.```

3. REMAINING WORKLOAD: **SMALL**

  * Support Hw/Sw to fix remaining issues.

4. CRITICAL ISSUES [list keys issues and action plans]

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_ETH_18G: Gen traffic 1 shot with random length 64-9600, Pkt always gen with 60 Bytes][O7-54] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 2 | [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 3 | [ATT_ETH_18G: Support Check Flow Per Port][O7-48] | nguyenht@atvn.com.vn | nan | Recheck on the latest version, but raised cafe on err field. Therefore, re-assign to aNguyenHT to recheck it|
| 4 | [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 5 | [ATT_ETH_Tester_8a0e0009: 10G Eth port alarm always UP][O7-40] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|


5. MILESTONES

  * Final project: ```Fixed all issues, Plan: TBD, aNhan will provide it.```


# Friday, April 10, 2020

1. STATUS: **<span style="color:YELLOW">YELLOW**

  * **<span style="color:GREEN">This project is in phase wrap-up**. We are working to clear all issues. (Currently, the total issue is 9. It's including the external issue).

2. KEY ACCOMPLISHMENTS [Compared to previous report]

  * **<span style="color:GREEN">DV and other teams are hard working to fix many issues last time.**

3. REMAINING WORKLOAD: **MEDIUM**

  * Support Hw/Sw to fix remaining issues.

4. CRITICAL ISSUES [list keys issues and action plans]

|Num. |Titile |Owner - Email |Plan |Action |
| ------ | ------ | ------ | ------ | ------ |
| 1 | [ATT_ETH_18G: Gen traffic 1 shot with random length 64-9600, Pkt always gen with 60 Bytes][O7-54] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 2 | [ATT_ETH_18G: Run full 4k flow, traffic has not well function with many time configure.][O7-53] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 3 | [ATT_ETH_18G: Support Check Flow Per Port][O7-48] | dangtv@atvn.com.vn | nan | I will try it on next week|
| 4 | [ATT_ETH_Tester_8a0e0009: New request to support FCS ERR PKT][O7-42] | dangtv@atvn.com.vn | nan | I will try it on next week|
| 5 | [ATT_ETH_Tester_8a0e0009: Force LOS on 1G port but it's Up, and vice versa][O7-41] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|
| 6 | [ATT_ETH_Tester_8a0e0009: 10G Eth port alarm always UP][O7-40] | nguyenht@atvn.com.vn | nan | wait for Hwer to check it|


5. MILESTONES

  * Final project: ```Fixed all issues, Plan: TBD, aNhan will provide it.```


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

  [O7-54]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000005415138>
  [O7-53]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000005402377>
  [O7-52]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000005116047>
  [O7-48]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004970083>
  [O7-44]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004935179>
  [O7-43]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004917118>
  [O7-42]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004890053>
  [O7-41]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004890030>
  [O7-40]:<https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#buginfo/403027000002130382/403027000004890007>
