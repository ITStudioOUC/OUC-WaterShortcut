# OUC-WaterShortcut
通过stream抓取海大e卡通的接口，把饮水机开关接口独立拆分，并使用快捷方式调用



## 前言

每次喝水都要打开海大e卡通——扫码，十分麻烦，秉持着召召哥的原生思想，把喝水开关给搬到快捷指令上来了，喝水就十分的方便。



## 准备工作

通过链接[下载](https://www.icloud.com/shortcuts/ec72180e14764a3897ffe76d22134ba0)快捷方式，或者下载仓库的`.shortcut`文件。

打开快捷方式，可以看到一些需要补充的信息

<img src="https://cdn.lmark.cc/img/image-20240707150710050.png" alt="image-20240707150710050" style="zoom:67%;" />

这里有两个词典，第一个词典填写个人信息，第二个填写你经常喝水的饮水机编号。接下来详细解释每个参数的获取

### ano

你的智能卡卡号，这个可以在很多地方获取到，这里推荐打开**海大e卡通->卡片挂失/解挂**就能找到

<img src="https://cdn.lmark.cc/img/86224976d0552f0ccbc207837ab872a.jpg" alt="86224976d0552f0ccbc207837ab872a" style="zoom:50%;" />



### balance和costmoney

balance是你打水时显示在屏幕上的金额，这个值以分为单位，只用于显示，可以随便填写；costmoney是每次点了开关之后，出水的最大金额，也是以分为单位



### info

这个需要通过抓包得到，IOS用户可以通过Stream来抓包，在打开扫码打开饮水机时，会通过info拿到一个token，其中token是会过期的，但是这个info不会。所有我们需要抓取info。但是开了代理之后，海大e卡通就打不开各种应用，这是就需要我们先打开扫码，去随便扫一个饮水机

<img src="https://cdn.lmark.cc/img/2558c3663ea91f0dad028f22721ad71.jpg" alt="2558c3663ea91f0dad028f22721ad71" style="zoom:50%;" />

此时，打开stream抓包，再回到此页面。开关一下饮水机。可以看到抓包记录里多了两条GetToken记录（下图红框）：

<img src="https://cdn.lmark.cc/img/1c55cbf0b66030c34ec2c2b681a04d1.jpg" alt="1c55cbf0b66030c34ec2c2b681a04d1" style="zoom:50%;" />

将随便一个info填入快捷指令的info中即可





### 饮水机编号

第二个词典可以存放常用的一些饮水机编号，还可以自定义名字，这个编号就是饮水机小屏幕上的编号，一台饮水机通常有两个编号，一冷一热，编号是相邻的。比如13458就是综合体南楼四楼的饮水机的冷水；13459是热水。



## 使用

填写完以上信息就可以用了运行快捷指令后，选择对应的饮水机就可以使用了

<img src="https://cdn.lmark.cc/img/fe020d0b0417e9a7a3a54e8d299d7ca.jpg" alt="fe020d0b0417e9a7a3a54e8d299d7ca" style="zoom:50%;" />



## 优势

- 便捷，不用每次打开海大e卡通扫码

- 极限，当你卡里钱少于1元还能使用

- 远程，可以在别人打水的时候关掉

  

## 贡献指南

我们欢迎所有形式的贡献，包括但不限于：

- 报告Bug
- 提出新功能建议
- 完善文档

请提交issue或pull request来参与项目改进。欢迎学弟学妹们提出意见和增加功能。

## 免责声明



本扩展仅供学习交流使用，请勿用于任何非法用途。使用本快捷方式所产生的一切后果由用户自行承担。

## 许可证



本项目采用 [MIT 许可证](https://github.com/ITStudioOUC/OUC-JWGL-Helper/blob/master/LICENSE)。

## 联系方式



如有任何问题或建议，请通过以下方式联系我们：

- 提交GitHub Issue
- 发送邮件至：[admin@itstudio.club](mailto:admin@itstudio.club)

感谢您对OUC喝水助手的支持！
