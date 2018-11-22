# Readme
***
## 准备工作  
按照TaskA中的步骤，启动zookeeper和kafka服务，并创建一个名为kafka-test的topic。
## 配置环境
在pom.xml中添加依赖。  
![img3](img3.png)
## 测试
分别运行ProducerDemo和ConsumerDemo，ConsumerDemo在控制台输出之前ProducerDemo发送的信息即表明测试成功。
