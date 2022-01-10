# 基于scapy编写端口扫描器

## 实验要求

1.禁止探测互联网上的 IP ，严格遵守网络安全相关法律法规
2.完成以下扫描技术的编程实现
TCP connect scan / TCP stealth scan
TCP Xmas scan / TCP fin scan / TCP null scan
UDP scan
上述每种扫描技术的实现测试均需要测试端口状态为：开放、关闭 和 过滤 状态时的程序执行结果
提供每一次扫描测试的抓包结果并分析与课本中的扫描方法原理是否相符？如果不同，试分析原因；
在实验报告中详细说明实验网络环境拓扑、被测试 IP 的端口状态是如何模拟的
（可选）复刻 nmap 的上述扫描技术实现的命令行参数开关

## 实验环境
1. Virtualbox

2. python 3.9

2. scapy 2.4.3

3. nmap 7.80

4. Linux kali 5.7.0-kali1-amd64

实验虚拟机网卡配置

1.攻击者主机
172.16.222.129

08:00:27:00:b0:b9

2.靶机
172.16.222.144

08:00:27:22:9c:67

3.网关
172.16.222.1

08:00:27:07:25:95

## 实验步骤

输入sudo apt-get install ufw

安装ufw


用sudo ufw status检查ufw状态，若为inactive,则是未启动
#启用
sudo ufw enable
#禁用
开房22和80端口

分别在端口开房、关闭、过滤时运行附件中的代码文件