# raspberrypi_api
把树莓派的硬件功能作为web api

![](http://oav6fgfj1.bkt.clouddn.com/ledf96a0f7d.png)

# 原因
*  近期公司有一个有趣的项目，希望用乐高玩具式的可视化编程工具来操控硬件
*  树莓派操控硬件需要有root权限，作为服务之后则没有限制
*  解耦

# 架构
*  初期效用flask作为web框架
*  把led_server视为下位机，api视为指令集

# 使用
我的树莓派当前ip为：192.168.0.106

### 启动服务
sudo python led_server.py

### 控制
可以在浏览器或命令行里打开api接口（动作）

*  点亮红灯： curl 192.168.0.106/led_up
*  熄灭红灯： curl 192.168.0.106/led_down
*  闪啊闪  ： curl 192.168.0.106/led_up_down


# 微信控制
和此前的wechat_bot关联即可

# todo
*  权限
*  cors 允许网页内控制