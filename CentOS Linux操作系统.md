# CentOS Linux操作系统

## 虚拟机软件

虚拟机（Virtual Machine）指通过软件模拟的**具有完整硬件系统功能**的、运行在一个完全隔离环境中的**完整计算机系统**。通过虚拟机可以在一台计算机上同时运行多个操作系统。

常见的用于桌面计算机的虚拟机软件有 **VirtualBox、VMware、Workstation、Microsoft Windows Virtual PC** 等。

**VMware Workstation** 是由全球著名云计算基础架构解决方案提供商威睿（Virtual Machine ware，VMware）公司出品的一款虚拟化产品，是目前实现**虚拟化程度最高、应用最广泛**的虚拟化产品。

## 虚拟机网络

VMware Workstation 虚拟机提供三种网络通信方法：

1. **桥接模式**

   VMware Workstation 提供一台名为 VMnet0 的虚拟交换机，实现物理机和虚拟机进行通信，虚拟机网卡与物理机网卡必须处在相同网段，虚拟机可以通过物理机的物理网络访问互联网。

   **缺点**：占用物理机的局域网IP地址资源

2. **NAT模式**

   VMware Workstation 提供一台名为 VMnet8 的虚拟交换机，以及生成了一个虚拟路由器作为 NAT 设备用于连接虚拟机和物理机所在的两个不同的网段，通过虚拟路由器（NAT）将不同网段的数据转发到另一个网段中以实现不同网段相互通信的目的，虚拟机可以通过物理机的物理网络访问互联网。

   **优点**：节约占用物理机的局域网IP地址资源

3. **仅主机模式**

   VMware Workstation 提供一台名为 VMnet1 的虚拟交换机，实现物理机和虚拟机进行通信，与 NAT 模式类似，但缺少 NAT 设备，虚拟机网卡与物理机网卡必须处在相同网段，虚拟机无法通过物理机的物理网络访问互联网。

## CentOS 概念

社区企业操作系统（Community Enterprise Operating System，**CentOS**）是 Linux 的发行版之一，它由 RedHat 公司发行的 Linux 企业版（RedHat Enterprise Linux）依照开源协议编译而成的。CentOS 是一款**完全开源及免费**的操作系统。

## CentOS 在 VMware Workstation 上安装与配置

**略······**

## 小结

CentOS 是众多 Linux 操作系统发行版中比较优秀的一款免费开源产品，它提供了对 OpenStack 的官方支持，且具有服务器所需的稳定性与可靠性高的特点，同时提供了对OpenStack安装包的官方下载，因此  OpenStack 云计算平台通常是构建在CentOS Linux操作系统之上的。