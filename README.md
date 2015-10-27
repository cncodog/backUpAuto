# backUpAuto

本项目为dockerclub创建自动化运维脚本

计划维护脚本包括
 1、blog社区的mysql库在线备份，自动保存至云平台
 2、实现社区问答平台的mongod库的在线备份，自动保存至平台
 3、实现社区所有七牛云存储的在线备份工作
 4、云服务器备份后，考虑采取制作镜像的方式生成镜像（后期处理）

##脚本使用
1、修改/etc/crontab #添加计划任务
2、vi /etc/crontab #在下面添加
3、30 1 * * * root /****.sh #表示每天凌晨1点30执行备份
4、重新启动crond使设置生效
  /etc/rc.d/init.d/crond restart
  chkconfig crond on #设为开机启动
  service crond start #启动
##七牛备份方案
http://www.cnblogs.com/tanhehe/p/4264181.html

# 版权 & 协议

Copyright (c) 2013-2015 DockerClub Foundation - Released under the [MIT license](LICENSE).
