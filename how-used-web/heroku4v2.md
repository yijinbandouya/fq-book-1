# heroku搭建v2ray服务器

 fork！github项目：

* [v2hero](https://github.com/onplus/v2hero)

使用现成的[模板](https://heroku.com/deploy?template=https://github.com/onplus/heroku_go-getting-startedhttps://heroku.com/deploy?template=https://github.com/onplus/heroku_go-getting-started)，默认的uuid有冲突所以需要更改

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_073517.png)

使用[uuidgenerator](https://www.uuidgenerator.net/)刷新一次页面每次均生成不同uuid

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_073839.png)

复制uuid粘贴进入uuid填写空中并确定

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_080047.png)

授权登录[travis-ci](https://travis-ci.org/profile)中开启按钮并设置

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_074407.png)

在`setting`选项中找到`Environment Variables`

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_080618.png)

填入相应数据

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_081238.png)

关于`api key`的位置，点击头像选择`account setting`往下拉即可看到

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_081848.png)

按步骤构建即可

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_082146.png)

等待片刻，黄色变成绿色即可

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_082553.png)

`more`选项中选择`Restart Dynos`并再次选择就行

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_083502.png)

`view logs`确认启动成功

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_083035.png)

以v2rayN为例

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_090353.png)

填入相应的配置参数并确定

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_090615.png)

右键设置为活动服务器

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_091318.png)

测试

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/images/2018-05-16_093822.png)



