# heroku搭建ss服务器

> **[warning] 免费配额与限制：**

> * Network Bandwidth/流量: 2TB/month – Soft
> * Shared DB processing/并发数: Max 200msec per second CPU time – Soft
> * Dyno RAM usage/使用运行内存: 512MB – Hard
> * Slug Size/存储空间: 300MB – Hard
> * Request Length/请求时间: 30 seconds – Hard

> 在正确部署的情况下提示Application error，是由于访问量各项配额耗尽而停止服务

 fork！github项目：

* [shadowsocks-heroku](https://github.com/onplus/shadowsocks-heroku)

创建App

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-04-29_195722m.png)

起个可用名称，默认美国服务器就行，总之不要选网络有限制国家的服务器

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_013449m.png)

在`deploy`点击github图标，并搜索fork过来的项目名称`shadowsocks-heroku`

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_014155.png)

点击`Connect`按钮

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_014818.png)

转到`settings`点击` reveal config vars`

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_015444.png)

填入`METHOD`与`KEY`并设置其相关参数，关于各项加密算法请看此章结尾处

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_020104.png)

回到`deploy`选项

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_020653.png)

下拉点击`enable automatic deploys`完成后再点击`deploy branch`

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_020817.png)

此时已经部署成功了

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_021041.png)

[下载相关客户端](https://github.com/onplus/shadowsocks-heroku/releases)

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_021835.png)

下载完成后解压缩，并打开`config.json`配置文件

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_022113.png)

配置`config.json`填入页面生成的地址以及在heroku上设置好的加密与密码参数

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_022758.png)

再打开`ss-h.exe`与配置chrome代理插件`switchyomega`的各项参数，并应用选项

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_023617.png)

再选择已配置好的情景代理模式`proxy`

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_024447.png)

测试

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_025046.png)


加密算法

* rc4
* rc4-md5
* table
* bf-cfb
* des-cfb
* rc2-cfb
* idea-cfb
* seed-cfb
* cast5-cfb
* aes-128-cfb
* aes-192-cfb
* aes-256-cfb
* camellia-256-cfb
* camellia-192-cfb
* camellia-128-cfb

