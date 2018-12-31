# Kubernetes配置
***
# 准备工作
## 操作系统
* Ubuntu 16.04 LTS
## 环境配置
## 安装Docker、Docker.io
    sudo apt-get install docker
    sudo apt-get install docker.io
## 关闭selinux、firewall、swap，写配置文件 
    systemctl stop firewalld && systemctl disable firewalld
    swapoff -a
    setenforce 0
    cat <<EOF >  /etc/sysctl.d/k8s.conf
    net.bridge.bridge-nf-call-ip6tables = 1
    net.bridge.bridge-nf-call-iptables = 1
    EOF
