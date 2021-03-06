# 通过微信网页api收集微信群聊天记录

* 背景

由于我们公司目前产品的信息都是通过人工录入的，在时效性和准确性上都有一定的折扣，在和同事们讨论过之后，决定采用通过网页版微信api来采集在各个金融微信g群中的聊天记录，再通过自然语言分析进行产品库的扩充．

* 微信web版本

这篇文章介绍了[微信web版登陆的全过程](http://www.tanhao.me/talk/1466.html/)，微信web端的登陆本质上就是通过访问服务器分配的会话ID去获得登陆的二维码，我们在这个项目中用到微信机器人就是通过这个api进行开发的．


* 微信机器人

开源项目[wxbot](https://github.com/liuwons/wxBot)
，本质是一个微信web版的ＡＰＩ.这个项目所有的逻辑都在ＷＸＢot这个类中，通过改写这个类的不同方法，我们可以取到登陆微信账号联系人，聊天信息，群组，公众号等信息．

在收集金融群信息的过程中，我主要重写了handle_msg_all这个方法，判断消息是否为群消息，再将群消息存入数据库．

注意wxbot这个项目中WXBot类　使用的是old　style 不可以使用super方法！

![deadeadea](https://www.jianguoyun.com/c/tblv2/CLjyGBIgulfdHVYmY8uNENC48-RXz8AIyBBz16jOpy_JQYyXG8Q/56jwgOMsPUQ/l)

* 部署与使用

为了可以随时控制微信机器人是否继续抓取消息，我选择了用supervisor来控制，在部署django的server之后，启动supervisor.(即在manage.py的同级目录下输入supervisord)会发现在当前目录下生成了qr.png文件．（如果你是在本地运行的会发现qr.png文件被自动打开了）这个qr.png文件就是根据本次会话id生成的二维码，用微信扫描这个二维码之后就可以登陆了，于此同时所有的群聊天记录都会被记录．













