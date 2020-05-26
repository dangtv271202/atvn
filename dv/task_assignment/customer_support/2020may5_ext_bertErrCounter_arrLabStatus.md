[![Arrive](https://raw.githubusercontent.com/dangtv271202/atvn/master/ArriveTechLogoBlue.png)](https://www.arrivetechnologies.com)

# Purpose

Cisco report an issue about "BERT Sync and BERT Error counter Issues"
```
Hi Team,


Please find below issues in BERT Engine Sync and Error Count, and please give your inputs on the same, PFA for the logs.

    1. BERT NOT sync for E1 Framed SAToP on 48T1E1 card.
    2. Mode de1 - Error counter is not updated as expected value, it always giving greater than expected value for 20CS cards.
```

# Arive lab
> 1. BERT NOT sync for E1 Framed SAToP on 48T1E1 card.

AIS is raising. Therefore, that's impacting to PRBS bert engine. Could u clear it first, then check prbs engine?

> 2. Mode de1 - Error counter is not updated as expected value, it always giving greater than expected value for 20CS cards.

May 12, 2020: Based on Cisco's inform, we tried to replicate this case in Arrive lab but not successfully. Therefore, @Cisco team: Please replicate it and send us the webex link, Arrive team will join to debug it with u.
The status in Arrive lab as below:

```
Source REV      : On gitcommit=heads/test/product/cisco_autotest-0-g355931771a8d45b222b20df7be393b2ffd62fc92
Driver Version  : 4.5.0.b005 (active) (Includes 2.6.26.b003)
Hardware Version:
+------+------------+---------------------------------+----------+
|      |            |                                 |          |
|Device|Product code|Version                          |HAL       |
|      |            |                                 |          |
+------+------------+---------------------------------+----------+
|1(*)  |0x60210071  |4.7 (on 2019/08/07), built: 10.80|0x4ab01000|
+------+------------+---------------------------------+----------+
AT SDK >prbs engine force single 1 100
AT SDK >
AT SDK >show prbs engine counters 1 r2c
+------------+--------+-------+-------+-------+-----+----------+-------------+------------------+-------+------+-----------+------------+
|            |        |       |       |       |     |          |             |                  |       |      |           |            |
|Channel     |engineId|txFrame|TxBit  |rxFrame|RxBit|RxBitError|RxBitLastSync|RxBitErrorLastSync|RxSync |RxLoss|RxLostFrame|RxErrorFrame|
|            |        |       |       |       |     |          |             |                  |       |      |           |            |
+------------+--------+-------+-------+-------+-----+----------+-------------+------------------+-------+------+-----------+------------+
|de1.10.1.1.1|1       |N/A    |7349768|N/A    |N/A  |100       |N/A          |N/A               |7349652|0     |N/A        |N/A         |
+------------+--------+-------+-------+-------+-----+----------+-------------+------------------+-------+------+-----------+------------+
AT SDK >
AT SDK >
AT SDK >show pdh de1 10.1.1.1.1
+------------+------------+----------+------------+----------+------------+---------+-------+------------+---------+--------------+--------------+---------+-------+------+-------+-------+----+--------+------------+
|            |            |          |            |          |            |         |       |            |         |              |              |         |       |      |       |       |    |        |            |
|DE1 ID      |FramingMode |TimingMode|TimingSource|clockState|HwClockState|Signaling|DS0List|LoopbackMode|Interrupt|ForcedTxAlarms|ForcedRxAlarms|Led State|Bound  |Enable|autoRai|autoAis|Idle|IdleCode|LosDetection|
|            |            |          |            |          |            |         |       |            |         |              |              |         |       |      |       |       |    |        |            |
+------------+------------+----------+------------+----------+------------+---------+-------+------------+---------+--------------+--------------+---------+-------+------+-------+-------+----+--------+------------+
|de1.10.1.1.1|ds1_unframed|system    |none        |N/A       |0           |dis      |None   |release     |None     |None          |None          |off      |satop.1|en    |en     |en     |dis |0x17    |dis         |
+------------+------------+----------+------------+----------+------------+---------+-------+------------+---------+--------------+--------------+---------+-------+------+-------+-------+----+--------+---------
```
