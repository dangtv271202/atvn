# Arrive Technologies

[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)


# Estimate resource

## Trinh Van Dang

* Total workload: ```>100%```
* Full control QA for 10GMS cisco AF6CCI0071: List Sw items and transfer task for member and check it also. Check the new FPGA with update "interrupt restore", sum status, Support customer, ...
  - Next release:
    + Update ``` restore based on version 5.0```: May 5, 2020; On-track
    + Update ```FEAC```: This case is applying full Cisco cards. About the 10GMS Cisco, it's not ready yet. Hope release it May 11, 2020.
    + Wrap-up this project with ```CEM + Imsg/Ppp```: Plan ```TBD```
  - Testing BERT, define a full mix test-cases with full services.
  - Take about ```80% workload```
* MRO 20G/10G wCAS: Full control QA for this project
	- Ticket 101: Support aVC/Onder to debug this issue
	- Take about ```5% workload```
* 10GMS Ciena AF6CNC0071: Support c.Hoa's team to confirm some Epass issues. Take about ```10% workload```
* ATT_ETH_18G/ATT: Confirm some issues from SW/HW. Take about ```10% workload```

## Nguyen Van Bang

* Total workload: ```To be define.```
* He is mainly working to research ```"MACsec" Technologies```. Currently he is sharing full workload on this task. BTW, I don't control this task, he is reporting to aMinh directly. Therefore, get his report for more inform task.

## Pham Minh Truong

* Total workload: ```>100%```
* He's mainly working on 10GMS project. We having a next release May 05, 2020 to update ```Interrupt restore based on version 5.0```. Thereofore, he is helping me to QA many functionals:
  - ```Interrupt tree/restore```: Full QA, SDH: ```53 testcase for each path (total 14 paths) = 742 testcase```. Finish it before Final release. Status: on-track.
  - ```FAST SEARCH```: Fast QA, manual with some channels and some paths. Take note that it must run with manual case (ATT is not support to check auto-test). He takes ```a day``` to finish it.
  - ```Pm/Fm, interrupt tree, DCC, mixing with TOH```: Fast QA, Finish before Final release. Status: on-track.
  - Support Hw/Sw to fix remaining issues: MTU counter, ... (```TBD```, some cases are can't define plan time, stuck at HWer).
  - Share 0.5 day ```(About 15% workload)``` to QA new item SDK: MRU update on HDLC and he will confirm it on DCC service.
  - He's sharing ```> 100% workload``` to QA this project.
* Other tasks: Support ATT team to confirm issue, ... Plan: ```TBD```

## Nguyen Minh Quang

* Total workload: ```TBD```
* He's mainly working on 10GMS project. We having a next release May 05, 2020 to update ```Interrupt restore based on version 5.0```. Therefore, he is helping me to QA many functionals:
  - Imsg for full paths: Fast QA, but scan many test-cases in this function ```(520 test-cases)```. Take note that some issues are impacting to QA Imsg service (MPEG, PDA hang-out, must reload FPGA to recover traffic, it takes about 10-15min/load FPGA). Finish it before Final release. Status: on-track.
  - Mix CEM: Fast QA, but scan many test-cases in the mix test-cases ```(CEP: 134, Satop: 127, CESOP: 171)```. Finish before Final release. Status: on-track.
    + He takes ```5%``` to run auto-test model.
    + Analyze issue (if have): Share about ```40%``` workload, set high priority if this case is happens.
      + Backup task: ```Define a mix test-case service with full service```. If run // with analyze task, take about ```35%``` workload.
    + He keeps 3 model test to QA parallel this time. Some mix issues (auto-test) takes ```lots of time``` to analyze it.
  - BTW, he is sharing his time to support HW/SW fix all remaining issues to wrap-up project. (```TBD```, some cases are can't define plan time, stuck at HWer).
  - Share 0.5 day ```(About 20% workload)``` to QA new item SDK: MRU update on HDLC and he will confirm it on IMSG service.
  - Share time to debug customer (```if have, TBD```)
  - Totally, he will share ```> 100% workload``` to QA this project.
* Take time to finish research ```MACsec```: ```TBD```, I don't control it. Please get his status/plan from mr.Minh/Bang.
* 20G MRO: Share time to scan ```warm restore``` with auto test if aNam finish task update ... Workload: ```TBD```
