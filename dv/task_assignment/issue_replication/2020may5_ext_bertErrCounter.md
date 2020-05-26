1.TASK NAME: Issue Replication

2.TASK DESCRIPTION:
Provide general task information:
 - Cisco report an issue about "BERT Sync and BERT Error counter Issues" via email.
 - Firstly Truong will replicate it in Arrive lab. After that, we will work with customer later.
 - The version, configuration,... as below:

```
 AT SDK >

AT SDK >show driver

Driver Version  : 4.4.9.b008 (active) (Includes 2.6.26.b003 + 4.4.9.patch.6)

Hardware Version:

+------+------------+---------------------------------+----------+
|      |            |                                 |          |
|Device|Product code|Version                          |HAL       |
|      |            |                                 |          |
+------+------------+---------------------------------+----------+
|1(*)  |0x60210071  |4.7 (on 2019/08/07), built: 10.80|0x8a66a000|
+------+------------+---------------------------------+----------+

AT SDK >
 AT SDK >
 AT SDK >show pdh de1 10.1.1.1.1
 +--------------+------------+----------+------------+----------+------------+---------+-------+------------+-------------------------+--------------+--------------+---------+-------+------+-------+-------+----+--------+------------+
 |              |            |          |            |          |            |         |       |            |                         |              |              |         |       |      |       |       |    |        |            |
 |DE1 ID        |FramingMode |TimingMode|TimingSource|clockState|HwClockState|Signaling|DS0List|LoopbackMode|Interrupt                |ForcedTxAlarms|ForcedRxAlarms|Led State|Bound  |Enable|autoRai|autoAis|Idle|IdleCode|LosDetection|
 |              |            |          |            |          |            |         |       |            |                         |              |              |         |       |      |       |       |    |        |            |
 +--------------+------------+----------+------------+----------+------------+---------+-------+------------+-------------------------+--------------+--------------+---------+-------+------+-------+-------+----+--------+------------+
 |de1.10.1.1.1.1|ds1_unframed|ext#1     |none        |N/A       |0           |dis      |None   |release     |bom-change|inband-loopcod|None          |None          |off      |satop.1|en    |en     |en     |dis |0x17    |dis         |
 +--------------+------------+----------+------------+----------+------------+---------+-------+------------+-------------------------+--------------+--------------+---------+-------+------+-------+-------+----+--------+------------+
 AT SDK >
 AT SDK >
 AT SDK >show pdh de1 alarm 10.1.1.1.1
 +--------------+-----+-----+-----+-----+-----+------+------+-----+------+------+-------+
 |              |     |     |     |     |     |      |      |     |      |      |       |
 |DE1 ID        |LOS  |LOF  |AIS  |RAI  |LOMF |SigLOF|SigRAI|Ebit |BER-SD|BER-SF|BER-TCA|
 |              |     |     |     |     |     |      |      |     |      |      |       |
 +--------------+-----+-----+-----+-----+-----+------+------+-----+------+------+-------+
 |de1.10.1.1.1.1|Clear|Clear|Clear|Clear|Clear|Clear |Clear |Clear|Clear |Clear |Clear  |
 +--------------+-----+-----+-----+-----+-----+------+------+-----+------+------+-------+
 AT SDK >
 AT SDK >
 AT SDK >
 AT SDK >show prbs engine counters 1-10 ro <<< expected 100
 +--------------+--------+-------+---------+-------+-----+----------+-------------+------------------+---------+------+-----------+------------+
 |              |        |       |         |       |     |          |             |                  |         |      |           |            |
 |Channel       |engineId|txFrame|TxBit    |rxFrame|RxBit|RxBitError|RxBitLastSync|RxBitErrorLastSync|RxSync   |RxLoss|RxLostFrame|RxErrorFrame|
 |              |        |       |         |       |     |          |             |                  |         |      |           |            |
 +--------------+--------+-------+---------+-------+-----+----------+-------------+------------------+---------+------+-----------+------------+
 |de1.10.1.1.1.1|1       |N/A    |370834808|N/A    |N/A  |93        |N/A          |N/A               |143827139|0     |N/A        |N/A         |
 +--------------+--------+-------+---------+-------+-----+----------+-------------+------------------+---------+------+-----------+------------+
 AT SDK >
 AT SDK >
 AT SDK >show prbs engine 1
 +--------+--------------+-------+-------+------------+------------+------+----------+---------+---------+----------+----------+-----+--------+-------+-------+
 |        |              |       |       |            |            |      |          |         |         |          |          |     |        |       |       |
 |engineId|channel       |txMode |rxMode |txFixPattern|rxFixPattern|invert|forceError|txEnabled|rxEnabled|txBitOrder|rxBitOrder|alarm|sticky  |genSide|monSide|
 |        |              |       |       |            |            |      |          |         |         |          |          |     |        |       |       |
 +--------+--------------+-------+-------+------------+------------+------+----------+---------+---------+----------+----------+-----+--------+-------+-------+
 |1       |de1.10.1.1.1.1|prbs20r|prbs20r|N/A         |N/A         |dis   |dis       |en       |en       |msb       |msb       |none |lossSync|tdm    |tdm    |
 +--------+--------------+-------+-------+------------+------------+------+----------+---------+---------+----------+----------+-----+--------+-------+-------+
 AT SDK >
 ```

3. RESOURCES REQUIRED:
 - DV-TruongPm is take this task.
 - Only use 1 board on system 38 (Loop-back SONET) to replicate it.

4. DELIVERABLES:
 - Status report: TruongPm will provide it after testing.
 - Zoho tracking: `None`

5. MILESTONES:
 - Breakdown the task into subtasks and milestones. Identify the effort, approximate duration and dependencies of each milestone: `None`
 - Start date: `May 12, 2020`
 - Due date:  `May 12, 2020`

6. COMPLETION CHECKLIST:
 - Status report.
 - Zoho tracking update for the issues.
 - Task tracking
 - Reviewed

7. REPORT RULE:
 - Update task status after finish testing and check with customer (If have).
