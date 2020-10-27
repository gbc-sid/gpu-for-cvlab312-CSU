### 创建一个容器

#### TODO

1. [建立端口映射](#建立端口映射)
2. [加载GPU](#加载GPU)
3. [关键项目安装教程](#关键项目安装教程)
4. **login and enjoy your owner container** :+1:

<br/>
<br/>

#### 建立端口映射

  1. **进入子容器container1**  
    `lxc exec container1 bash` 

  2. **查看容器**  
    `lxc list`  

  3. **记住该容器ipv4地址, 记作container1-ip**  

  4. **建立端口映射**  
    `sudo iptables -t nat -A PREROUTING -d gateway-ip -p tcp --dport Port -j DNAT --to-destination container1-ip`  
    `gateway-ip`: 路由器ip  
    `Port`: 给定容器端口(Server1:11000-13000, Server2:13000-15000, Server3:15000-17000, Server4:17000-19000)  

  5. **映射端口查询**  
    `sudo iptables -t nat -L --line-number`  

  6. **删除端口映射**  
    `iptables -t nat -D PREROUTING num`  
    `num`: 映射ID  

  7. **保存端口映射**  
     **_注：reboot之前一定要保存，否则映射会消失_**
    `sudo iptables-save > /etc/iptables/rules.v4`  
    

<br/>
<br/>

#### 加载GPU

`lxc config device add <container name> gpu gpu`

<br/>
<br/>

#### 关键项目安装教程

  1. **nvidia显卡驱动**   
    查看显卡驱动及编译器版本
    https://blog.csdn.net/s_sunnyy/article/details/64121826  
    **容器中安装显卡驱动不安装内核文件，否则会安装失败**  
    `sudo sh /NVIDIA-Linux-x86_64-xxx.xx.run --no-kernel-module`  

  2. **minconda3**
    安装及配置  
    https://ywnz.com/linuxjc/3834.html  
    安装之后无法识别conda命令   
    https://blog.csdn.net/qq_29007291/article/details/100516485

  3. **GCC**  
    sudo apt-get install gcc

  4. **CUDA10.0+Cudnn7.6.4**  
    安装及配置:    
    https://blog.csdn.net/qq_43030766/article/details/91513501?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.channel_param&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.channel_param   
    cudnn安装教程:  
    https://blog.csdn.net/Lucifer_zzq/article/details/76675239







