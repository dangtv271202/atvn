1.TASK NAME: Manual Onboard

2.TASK DESCRIPTION:
Provide general task information:
 - Test case list that needs to validate onboard.
  + Run full Pws (5k for Ds1 SAToP and 4k for E1 SAToP) and cover:
    + Configure min 64bytes SAToP with min JB
    + Configure min 64bytes SAToP with max JB
    + Configure min 64bytes SAToP with random in range JB
  + Mix SAToP (64bytes) with other services (CEP, CESoP, De3 SAToP)
 - Release timelines for refer: `2 days to test all test-cases`. If Ok, we will apply it for others: De1, De3, 3GMS, 10G, 5G CEM.
 - Test plan, Test model & Test procedures to follow: `Ref check normal traffic + JB test-cases`
 - Related TCL, TTL scripts to use: `Follow this task link: https://crmplus.zoho.com/arrivetechnologies/index.do/cxapp/projects/arrivetechnologies#taskdetail/403027000003095123/403027000005664071/403027000005766416`
 - Project database, source safe, zoho link, working database, point out related documents: `10GMS AF6CCI071`
 - Email to related people to have information about the task(If needed).
   + LD leader: `nhanngt@atvn.com.vn`
   + SW leader: `dungtn@atvn.com.vn`
   + DV team: `dangtv@atvn.com.vn, truongpm@atvn.com.vn, quangnm@atvn.com.vn`

3. RESOURCES REQUIRED:
- How many people are needed to complete the task: `10GMS DV team: Dangtv, TruongPm, QuangNm`
- Equipment list to use: Systems, testers, cables, SFP, Servers...: `10GMS card, MRO STM Tester + Some SFPs` to connect model

4. DELIVERABLES:
 - Functional/Full Validation Plan in excel format.
  + Traffic with full PW De1 SAToP
    - JB: min, max, in-range
  + Mix SAToP (64bytes) with other services (CEP, CESoP, De3 SAToP)
    - JB: min, max, in-range

5. MILESTONES: `Wait for a Nhan feedback, update later.`
 - Breakdown the task into subtasks and milestones. Identify the effort, approximate duration and dependencies of each milestone.
 - Provide timeline for the task or each sub-task(start date & due date)

6. COMPLETION CHECKLIST:
 - Document: Noted items if have.
 - Test results
 - Test report.
 - Detected issue list
 - Zoho tracking for the detected issues & their status.
 - Reviewed

7. REPORT RULE:
 - Update task status on everyday.
