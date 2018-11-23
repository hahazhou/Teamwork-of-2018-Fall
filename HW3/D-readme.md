# D:Design a scenario to demonstrate the streaming processing

## 方案简介
在producer中向input topic输入数字（温度），把topic中最大的数字输出到output topic。同时设置门槛：最大值必须大于20.
-----
## 实施方法
先创建input topic，用于输入温度数据。
命令为 bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic renrui-temp
然后创建output topic，用于存放最大值。
命令为 bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic renrui-temp-max
运行temperature.java
命令为 bin/kafka-run-class.sh com.examples.scenario.temperature
打开一个producer，向renrui-temp输入数据
命令为 bin/kafka-console-producer.sh --broker-list localhost:9092 --topic renrui-temp
打开一个consumer,从renrui-temp-max中读数据
命令为 bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic renrui-temp-max --from-beginning
-----
##要点
（1）假如输入的温度均不到20，则不会在output topic中读到数据。
（2）用ctrl-c结束程序
