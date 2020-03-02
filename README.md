# 虚拟机openwrt软路由搭建及网络设置 

**1.openwrt软路由介绍及搭建**  

**第一步**
虚拟机文件下载到电脑中解压缩，然后在VMware Workstation软件中选择文件菜单里的打开命令，找到刚才解压缩的文件，导入虚拟机(需要大概1.5G的硬盘空间)  
虚拟机文件下载链接: https://pan.baidu.com/s/1kWRZtQn 密码: 5qcj  

**第二步** 
导入虚拟机  
![1.导入虚拟机.png](/openwrt/1.导入虚拟机.png)  

**第三步** 
开启虚拟机  
![2.开启虚拟机.png](/openwrt/2.开启虚拟机.png) 

        输入vi /etc/config/network  
        修改网卡，网卡配置如下，按需修改lan以及wan口的IP。wq!保存  

第四步  
配置网络  
![3.配置网络.png](/openwrt/3.配置网络.png)  

        service network restart重启网卡 

  这里需要说明的是：  

        LAN口为内网口，WAN为外网口，这一步相当于，给软路由设定一个网关（LAN），WAN可直接将option proto设置成DHCP  

        因为openwrt有wan、lan口则需要两块网卡，如下：  

        第一块网卡是lan口网卡，处于31网段。  
        第二块网卡是wan口网卡，直接桥接。  

   **注意**：  
        在给虚拟机添加网卡的时候，openwrt虚拟机两块网卡顺序不能变，第一块为lan口网卡，第二块为wan口网卡  

![3.配置网络网卡顺序.png](/openwrt/3.配置网络网卡顺序.png)   




2.群晖系统的搭建  



3.win7系统搭建  


4.虚拟机网络配置  

![截图](a.png)  
