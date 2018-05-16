# 宿主机使用VM的代理

> **[warning]** **注：**

> * **在公网下同一局域网，所开启VPN的物理机可以通过热点形式共享全局的VPN网络**

> * **手机也能使用虚拟机所配置的本机代理服务器，不需要同PC机设置专属的VMware转发**

> * **宿主机使用代理可以不用向虚拟机设置额外的端口转发，只需添加代理的地址与端口即可**

> * **除默认配置的仅主机模式外，宿主机使用VPN会影响全局网络，虚拟机可以直接访问互联网**

> * **由于虚拟机是非全局性的独立的虚拟网络，使用VPN时并不能影响主机也能够网络访问互联网**

在NAT模式中，虚拟机通过宿主机器所在的公网网络来访问互联网（目前在墙内），vm使用代理软件转发端口监听任意地址，主机在代理中配置同一公网内的局域网IP与端口，完成网络之间的互联共享。以下是具体实例：

在NAT模式中不考虑使用VPN或代理的情况下，IP地址是完全一致的

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-13_005931.png)

在vm中开启v2ray以及配置privoxy相关参数`0.0.0.0:8118`监听任意地址开启的`8118`端口，将所有http流量再转发至本机代理

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-12_065612.png)

在vm设置代理本机地址与privoxy代理的监听端口

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-13_013525.png)

查看vm局域网地址

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-13_014622.png)

VMware设置端口映射

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-13_015340%20%281%29.png)

宿主机中设置代理，填入vm的IP地址与端口

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-13_020423%20%281%29.png)

测试

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-13_021830.png)




