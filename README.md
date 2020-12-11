# 1.树莓派安装ubuntu mate
链接：https://pan.baidu.com/s/1GQnNj2NCIrN6dyIxb9SjWg 
提取码：0spa 

# 2.安装ROS Kinetic
参考链接：
官方wiki：http://wiki.ros.org/cn/kinetic/Installation/Ubuntu
## 2.1配置 Ubuntu 软件仓库
在 `/etc/apt/sources.list` 文件中，将软件源的地址改为 `http://mirrors.ustc.edu.cn/ubuntu-ports`
以下是 Ubuntu 16.04 /etc/apt/sources.list 文件的参考配置内容：
```
deb https://mirrors.ustc.edu.cn/ubuntu-ports/ xenial main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu-ports/ xenial main main restricted universe multiverse

deb https://mirrors.ustc.edu.cn/ubuntu-ports/ xenial-updates main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu-ports/ xenial-updates main restricted universe multiverse

deb https://mirrors.ustc.edu.cn/ubuntu-ports/ xenial-backports main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu-ports/ xenial-backports main restricted universe multiverse

deb https://mirrors.ustc.edu.cn/ubuntu-ports/ xenial-security main restricted universe multiverse
deb-src https://mirrors.ustc.edu.cn/ubuntu-ports/ xenial-security main restricted universe multiverse
```

参考链接：
配置指南：https://help.ubuntu.com/community/Repositories/Ubuntu
中科院镜像配置指南：http://mirrors.ustc.edu.cn/help/ubuntu-ports.html
