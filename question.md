### 遇到过的问题

- **容器内输入nvidia-smi，GPU显示未加载**

    1.  Host输入`su -user`进入user用户  
    2.  `conda activate py3`激活py3环境, 依次输入  
        `import tensorflow as tf`  
        `tf.Session()`  
        来挂载GPU  

- **容器内输入nvidia-smi，GPU显示无法启动或不存在**

    查看linux系统内核是否更新，若更新，则进入管理账户，重新安装显卡驱动


- **xshell登录时输入不了密码， 只能输入公钥**  

    从Host进入容器配置sshd.config  
    https://www.jianshu.com/p/668427785760  

- **使用apt安装包时出现"E: Failed to fetch http://security.ubuntu.com/ubuntu/pool/main/l/linux/linux-libc-dev_4.15.0-121.123_amd64.deb  404  Not Found [IP: 91.189.88.142 80] "等类似错误**  

    运行`sudo apt-get update`更新地址

- **出现"failed call to cuInit"等类似问题**   

    禁用nouveau方法:  
    输入 `vi /etc/modprobe.d/blacklist.conf`  
    添加 `blacklist vga16fb`, `blacklist nouveau`, `blacklist rivafb`, `blacklist rivatv`, `blacklist nvidiafb`  
    执行 `sudo update-initramfs -u`  
    可通过命令 `lsmod | grep nouveau` 查看，一般无输出代表禁用成功  

- **pip下载超时问题**
    
    永久解决方案:  `pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple`

- **ibSM.so.6: cannot open shared object file: No such file or directory**

    `apt-get install libsm6`, `apt-get install libxrender1`

- **命令行禁用linux自动更新内核**

    `genee@reserva:~$ cat /etc/apt/apt.conf.d/10periodic`  
    `APT::Periodic::Update-Package-Lists` "1"  
    `APT::Periodic::Download-Upgradeable-Packages` "0"  
    `APT::Periodic::AutocleanInterval` "0"  
- **Ubuntu Linux内核版本升级或降级到指定版本（基于ubuntu 18.04示例）**

    https://blog.csdn.net/weixin_42915431/article/details/106614841?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-15.nonecase&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-15.nonecase

- **如果nvidia-smi只显示一部分卡**

    稍等一下，可能是GPU未挂载全

- **容器存储池不够，创建新的存储池**

    查看存储池并创建新池  
    `lxc storage list`  
    `lxc storage create pool_name zfs size=xxGB`  

    将pool改为pool_name
    `lxc profile copy default lxd`  
    `lxc profile list`  
    `lxc profile edit lxd`  

    相关网页：
    https://openwares.net/2019/08/08/lxd_zfs_storagepool/
    https://openwares.net/2019/08/13/lxd-change-storage-backend/








