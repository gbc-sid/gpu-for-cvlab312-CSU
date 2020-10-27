# gpu-for-cvlab312-CSU
 Introduction and tutorial of GPU server configuration in 312 Lab in Central South University   
 中南大学民主楼312实验室GPU服务器使用教程
<br/>
<br/>

### Administrator:   

**Bocong Gao 高博聪**    

**Shuanhu Di 邸拴虎**    

**Yimin Tang 唐一民**   

<br/>
<br/>

## Content
- [服务器系统介绍](#服务器系统介绍)
- [服务器当前状态](#服务器当前状态)
  - [Server1](#Server1)
  - [Server2](#Server2)
  - [Server3](#Server3)
  - [Server4](#Server4)
- [简易教程](#简易教程)
  - [LXD Container](/lxd.md)
  - [创建容器](/create.md)
- [Q&A 遇到过的问题](/question.md)


<br/>
<br/>

### 服务器系统介绍
 
| info | Server1 | Server2 | Server3 | Server4 | 
| :----: | :----: | :------: | :---: | :------: | 
| Port  | 11000 | 13000 | 15000 | 17000 | 
| gateway | 192.169.1.101 | 192.169.1.102 | 192.169.1.103 | 192.169.1.104 |
| 系统 | Ubuntu18.04 | Ubuntu18.04 | Ubuntu18.04 | Ubuntu18.04 | 
| GPU | GTX1080Ti * 4 | GTX1080Ti * 4 | RTX2080Ti * 4 | RTX2080Ti * 4 |  
| Nvidia drivers version | 430.26 | 430.26 | 430.26 | 430.26 |  
| conda | 4.7.12 | 4.7.12 | 4.7.12 | 4.7.12 | 
| CUDA | 10.0 | 10.0 | 10.0 | 10.0 |  
| CUDNN | 7.6.4 | 7.6.4 | 7.6.4 | 7.6.4 |  

<br/>
<br/>

### 服务器当前状态
#### Server1

| name | Account | Port | Login Name | Password | Ipv4 address |  
| :----: | :----: | :------: | :---: | :------: | :---: | :--------: |
|            | base | 11100 | root | 111 | 10.119.6.151:22 |
| Yimin Tang | tym | 11110 | root | 111 | 10.119.6.88:22 |
| Fuchang Han | hfc | 11120 | root | 111 | 10.119.6.155:22 |
| Siming Yuan | ysm | 11130 | root | 111 | 10.119.6.62:22 |
| Renzhong Wu | wrz | 11140 | root | 111 | 10.119.6.55:22 |
| Public | gongyong | 11150 | root | 111 | 10.119.6.38:22 |

#### Server2

| name | Account | Port | Login Name | Password | Ipv4 address |  
| :----: | :----: | :------: | :---: | :------: | :---: | :--------: |  
|   | base | 13100 | root | 111 | 10.88.221.23:22 |  
|   | gongyong | 13110 | root | 111 | 10.88.221.21:22 |  

#### Server3

| name | Account | Port | Login Name | Password | Ipv4 address |   
| :----: | :----: | :------: | :---: | :------: | :---: | :--------: |
|   | base | 15000 | root | 111 | 10.124.170.252:22 |
| Bocong Gao | gbc | 15100 | root | 111 | 10.124.170.74:22 |
| Shuanhu Di | dsh | 15110 | root | 111 | 10.124.170.91:22 |
| Pei Chen | cp | 15120 | root | 111 | 10.124.170.22:22 |
| Minghong Li | lmh | 15130 | root | 111 | 10.124.170.233:22 |
| Yezhan Zeng | zyz | 15140 | root | 111 | 10.124.170.178:22 |
| Xiaohui Ren | rxh | 15150 | root | 111 | 10.124.170.150:22 |
| Xuankang He | hxk | 15160 | root | 111 | 10.124.170.130:22 |
| Dong An | ad | 15170 | root | 111 | 10.124.170.24:22 |
| Xiaoyang Xiao | xxy | 15180 | root | 111 | 10.124.170.25:22 |
| Xiaoyu Yang | yxy | 15190 | root | 111 | 10.124.170.19:22 |

#### Server4

| name | Account | Port | Login Name | Password | Ipv4 address |   
| :----: | :----: | :------: | :---: | :------: | :---: | :--------: |
|   | test | 17001 | root | 111 | |
| Shaodi Yang | ysd | 17100 | root | 111 | 10.213.4.92:22 |
| Wuyang Chen | cwy | 17110 | root | 111 | 10.213.4.100:22 |
| Shuanhu Di | dsh | 17120 | root | 111 | 10.213.4.70:22 |
| Hui Wang | wh | 17130 | root | 111 | 10.213.4.84:22 |
| Wei Zhou | zw | 17140 | root | 111 | 10.213.4.74:22 |
| Wanan Zhang | zwn | 17150 | root | 111 | 10.213.4.134:22 |
| Yezhan Zeng | zyz | 17160 | root | 111 | 10.213.4.226:22 |
| Zhongyu Xie | xzy | 17170 | root | 111 | 10.213.4.54:22 |
| Jinna Yang | yjn | 17180 | root | 111 | 10.213.4.131:22 |

<br/>
<br/>






