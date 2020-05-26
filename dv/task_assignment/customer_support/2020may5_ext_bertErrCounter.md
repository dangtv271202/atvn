1.TASK NAME: Customer Support

2.TASK DESCRIPTION:
Provide general task information:
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
  - Truong help me to try it in Arrive lab.
  - I will work work Cisco in Cisco lab.

4. DELIVERABLES:

>> 1. BERT NOT sync for E1 Framed SAToP on 48T1E1 card.

> <Arrive/Dang>: AIS is raising. Therefore, that's impacting to PRBS bert engine. Could u clear it first, then check prbs engine?

<Cisco/Saravanakumar> still verification is in progress will let you know once verified.

> 2. Mode de1 - Error counter is not updated as expected value, it always giving greater than expected value for 20CS cards.

<Arrive/Dang>: No issue here. Saravanakumar will change his code and try again with IOS configure.


5. MILESTONES: `None`

6. COMPLETION CHECKLIST:
 - Support's status: No issue here, wait for Cisco update code and recheck on IOS version.
 - Action items: `None`
 - Support tracking: `None`
 - Task tracking: `None`
 - Reviewed: `None`


7. REPORT RULE:
 - `None`
