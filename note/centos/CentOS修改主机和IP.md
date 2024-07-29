* [一、修改主机名](#%E4%B8%80%E4%BF%AE%E6%94%B9%E4%B8%BB%E6%9C%BA%E5%90%8D)
* [二、修改 ip](#%E4%BA%8C%E4%BF%AE%E6%94%B9-ip)

---
# 一、设置主机名称

```bash
hostname "newhostname"		# 临时设置主机名

# CentOS6.x 编辑此配置文件 
vim /etc/sysconfig/network	

# CentOS7.x 编辑此配置文件 
vim /etc/hostname
		
# 输入新的主机名称	
newhostname	
				
vim /etc/hosts   			# 编辑配置文件
127.0.0.1 newhostname localhost  # 修改localhost.localdomaim
```

---
# 二、修改 ip

```bash
vim /etc/sysconfig/network-scripts/ifcfg-ens33 

TYPE=Ethernet
PROXY_METHOD=none
BROWSER_ONLY=no
DEFROUTE=yes
IPV4_FAILURE_FATAL=no
IPV6INIT=yes
IPV6_AUTOCONF=yes
IPV6_DEFROUTE=yes
IPV6_FAILURE_FATAL=no
IPV6_ADDR_GEN_MODE=stable-privacy
NAME=ens33
UUID=0a20f443-9c23-4274-a20f-c3f26d04f559
DEVICE=ens33
NM_CONTROLLED=no
ONBOOT=yes  #开启自动启用网络连接
BOOTPROTO=static  #启用静态IP地址
IPADDR=192.168.161.160 #设置IP地址
NETMASK=255.255.255.0  ##
GATEWAY=192.168.161.2  #设置网关
DNS1=192.168.161.2 #设置主DNS
```
