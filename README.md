## [urlooker][1]
监控web服务可用性及访问质量，采用go语言编写，易于安装和二次开发

## Feature
- 返回状态码检测
- 页面响应时间检测
- 页面关键词匹配检测
- 带cookie访问
- agent多机房部署，指定机房访问
- 检测结果支持向open-falcon推送

## ScreenShot

![看图][2]

![此处输入图片的描述][3]

![添加监控项][4]

## 上报项
- metric: url_status
- endpoint: url_id  (id为上图2中的id)
- tag: creator=creator
- counterType: GAUGE
- step: 60（可在配置文件设置）
- value: 0 (0~4 0表示正常，其他表示异常)

## Install

导入数据库
wget http://x2know.qiniudn.com/schema.sql
将schema.sql 导入数据库

二进制安装(Ubuntu 14.4 Go1.6下编译)：

    wget http://x2know.qiniudn.com/urlooker.tar.gz
    tar xzvf urlooker.tar.gz
    cd urlooker
    web/control start
    alarm/control start
    agent/control start

打开浏览器访问 http://127.0.0.1:1984 即可


源码安装及详细介绍见：
[https://github.com/urlooker][5]

## Thanks
一些功能参考了open-falcon，感谢 [UlricQin][6] & [laiwei][7]


  [1]: https://github.com/urlooker
  [2]: http://x2know.qiniudn.com/urlooker1.png
  [3]: http://x2know.qiniudn.com/urlooker3.png
  [4]: http://x2know.qiniudn.com/urlooker2.png
  [5]: https://github.com/URLooker/wiki
  [6]: http://ulricqin.com/
  [7]: https://github.com/laiwei