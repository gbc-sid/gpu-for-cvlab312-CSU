# gpu-for-cvlab312-CSU
 Introduction and tutorial of GPU server configuration in 312 Lab in Central South University
# 中南大学民主楼312实验室GPU服务器使用教程
<br/>
<br/>
administrator: **Bocong Gao 高博聪** **Shuanhu Di 邸栓虎**  **Yimin Tang 唐一民** 
<br/>
<br/>

## 目录
- [服务器系统介绍](#服务器系统介绍)
- [服务器当前部署](#服务器当前部署)


### 服务器系统介绍

| info | Server1 | Server2 | Server3 | Server4 |
| --- | --- | --- | --- | --- | --- | --- |
| Port | 11000 | 13000 | 15000 | 17000 |
| gateway | 192.169.1.101 | 192.169.1.102 | 192.169.1.103 | 192.169.1.104 |
| 系统 | Ubuntu18.04 | Ubuntu18.04 | Ubuntu18.04 | Ubuntu18.04 |
| GPU | GTX1080Ti * 4 | GTX1080Ti * 4 | RTX2080Ti * 4 | RTX2080Ti * 4 |
| Nvidia drivers version | 430.26 | 430.26 | 430.26 | 430.26 |
| conda | 4.7.12 | 4.7.12 | 4.7.12 | 4.7.12 |
| CUDA | 10.0 | 10.0 | 10.0 | 10.0 |
| CUDNN | 7.6.4 | 7.6.4 | 7.6.4 | 7.6.4 |

<br/>
<br/>

### 服务器当前部署
#### Server1

| 姓名 | 账号 | 登录IP | 端口 | 登录名 | 密码 | Ipv4地址 |  
| ---- | ---- | ------ | --- | ------ | --- | -------- |
|   | base | 202.197.66.3 | 11100 | root | 111 | 10.119.6.151:22 |
| 唐一民 | tym | 202.197.66.3 | 11110 | root | 111 | 10.119.6.88:22 |
| 韩付昌 | hfc | 202.197.66.3 | 11120 | root | 111 | 10.119.6.155:22 |
| 苑思明 | ysm | 202.197.66.3 | 11130 | root | 111 | 10.119.6.62:22 |
| 邬任重 | wrz | 202.197.66.3 | 11140 | root | 111 | 10.119.6.55:22 |
| 公用 | gongyong | 202.197.66.3 | 11150 | root | 111 | 10.119.6.38:22 |

#### Server2

| 姓名 | 账号 | 登录IP | 端口 | 登录名 | 密码 | Ipv4地址 |  
| ---- | ---- | ------ | --- | ------ | --- | -------- |
|   | base | 202.197.66.3 | 13100 | root | 111 | 10.88.221.23:22 |
|   | gongyong | 202.197.66.3 | 13110 | root | 111 | 10.88.221.21:22 |

#### Server3

| 姓名 | 账号 | 登录IP | 端口 | 登录名 | 密码 | Ipv4地址 |  
| ---- | ---- | ------ | --- | ------ | --- | -------- |
|   | base | 202.197.66.3 | 15000 | root | 111 | 10.124.170.252:22 |
| 高博聪 | tym | 202.197.66.3 | 15100 | root | 111 | 10.124.170.74:22 |
| 邸栓虎 | hfc | 202.197.66.3 | 15110 | root | 111 | 10.124.170.91:22 |
| 陈佩 | ysm | 202.197.66.3 | 15120 | root | 111 | 10.124.170.22:22 |
| 李明鸿 | wrz | 202.197.66.3 | 15130 | root | 111 | 10.124.170.233:22 |
| 曾业战 | zyz | 202.197.66.3 | 15140 | root | 111 | 10.124.170.178:22 |
| 任晓辉 | rxh | 202.197.66.3 | 15150 | root | 111 | 10.124.170.150:22 |
| 何煊槺 | hxk | 202.197.66.3 | 15160 | root | 111 | 10.124.170.130:22 |
| 安栋 | ad | 202.197.66.3 | 15170 | root | 111 | 10.124.170.24:22 |
| 肖晓阳 | xxy | 202.197.66.3 | 15180 | root | 111 | 10.124.170.25:22 |
| 杨晓喻 | yxy | 202.197.66.3 | 15190 | root | 111 | 10.124.170.19:22 |

#### Server4

| 姓名 | 账号 | 登录IP | 端口 | 登录名 | 密码 | Ipv4地址 |  
| ---- | ---- | ------ | --- | ------ | --- | -------- |
|   | test | 202.197.66.3 | 17001 | root | 111 | |
| 杨少迪 | ysd | 202.197.66.3 | 17100 | root | 111 | 10.213.4.92:22 |
| 陈武阳 | cwy | 202.197.66.3 | 17110 | root | 111 | 10.213.4.100:22 |
| 邸栓虎 | dsh | 202.197.66.3 | 17120 | root | 111 | 10.213.4.70:22 |
| 王辉 | wh | 202.197.66.3 | 17130 | root | 111 | 10.213.4.84:22 |
| 周玮 | zw | 202.197.66.3 | 17140 | root | 111 | 10.213.4.74:22 |
| 张皖南 | zwn | 202.197.66.3 | 17150 | root | 111 | 10.213.4.134:22 |
| 曾业战 | zyz | 202.197.66.3 | 17160 | root | 111 | 10.213.4.226:22 |
| 谢仲宇 | xzy | 202.197.66.3 | 17170 | root | 111 | 10.213.4.54:22 |
| 杨金娜 | yjn | 202.197.66.3 | 17180 | root | 111 | 10.213.4.131:22 |