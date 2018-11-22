# Kafka的安装配置
***
## 准备工作
* 下载zookeeper：http://zookeeper.apache.org/releases.html#download  
这里我选择了3.4.13版本  
完成后解压到E://Kafka目录下
* 下载kafka：http://kafka.apache.org/downloads  
这里我选择了2.11-2.0.1版本  
完成后解压到E://Kafka目录下
## 修改配置文件
### zookeeper配置文件修改
使用notepad++打开zookeeper-3.4.13/conf文件夹中的zoo.cfg修改 
> dataDir=E:\\Kafka\zookeeper-3.4.13\\tmp
