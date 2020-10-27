### 简易教程

*相关操作需登录Host(宿主机)，如有必要请与管理员联系，Host上文件删除修改需谨慎*
*Host进行reboot操作后请等待一段时间*

#### LXD Container基本操作

reference:  
1. https://linuxcontainers.org/lxd/getting-started-cli/#lxd-client
2. https://blog.csdn.net/EverGlow_Lida/article/details/106062860?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-5.nonecase&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-5.nonecase



- 安装
'snap install lxd'
- 初始化(具体配置参考文档)
'lxd init'
- 创建容器
'lxc launch imageserver:imagename instancename'
e.g.
'lxc launch ubuntu:18.04 test'
- 停止容器
'lxc stop instancename'
- 启动容器
'lxc start instancename'
- 重启
'lxc start instancename'
- 删除
'lxc delete instancename'
- 进入容器
'lxc exec instancename bash'
- 退出容器
'root@containername:~# exit'
- 上传文件到Host
'lxc file pull instancename/path-in-container path-on-host'
- 上传文件夹到Host
'lxc file pull -r instancename/path-in-container path-on-host'
- 下载文件到容器
'lxc file push path-on-host instancename/path-in-container'
- 下载文件夹到容器
'lxc file push -r path-on-host instancename/path-in-container'
- 创建自定义容器镜像
创建之前需停止该容器
'lxc publish containername --alias imagename'
**创建成功后，可以直接通过镜像创建新的容器(减少重复操作，提升速度，每个容器都需的配置只需配置一次即可)**
配置成功之后，创建含有该配置容器
'lxc launch imagename instancename'
- 创建新的storage pool
'lxc storage create poolname zfs size=poolsize'