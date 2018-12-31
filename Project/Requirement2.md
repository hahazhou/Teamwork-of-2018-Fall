# Kubernetes配置
***
# 准备工作
## 操作系统
* Ubuntu 16.04 LTS
## 环境配置
## 关闭selinux、firewall、swap，写配置文件 
    1.systemctl stop firewalld && systemctl disable firewalld
    2.swapoff -a
    3.setenforce 0
