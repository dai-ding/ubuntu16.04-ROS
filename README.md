# 1.树莓派安装ubuntu mate
链接：https://pan.baidu.com/s/1GQnNj2NCIrN6dyIxb9SjWg   
提取码：0spa 

# 2.安装ROS Kinetic
__参考链接：__  
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

__参考链接：__  
配置指南：https://help.ubuntu.com/community/Repositories/Ubuntu  
中科院镜像配置指南：http://mirrors.ustc.edu.cn/help/ubuntu-ports.html

## 2.2添加 sources.list
```
sudo sh -c '. /etc/lsb-release && echo "deb http://mirrors.ustc.edu.cn/ros/ubuntu/ $DISTRIB_CODENAME main" > /etc/apt/sources.list.d/ros-latest.list'
```

## 2.3添加公钥
```
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```

## 2.4安装
更新软件包索引以生效。  
```
sudo apt-get update
``` 
在ROS中，有很多不同的库和工具。wiki官方提供了四种默认的配置来帮助你开始。也可以单独安装ROS包。  

+ 桌面完整版: (推荐) : 包含ROS、rqt、rviz、机器人通用库、2D/3D 模拟器、导航以及2D/3D感知
```
sudo apt-get install ros-kinetic-desktop-full
```

+ 桌面版安装: 包含ROS、rqt、rviz以及通用机器人函数库。  
```
sudo apt-get install ros-kinetic-desktop
```

+ 基础版安装: (简版) 包含ROS核心软件包、构建工具以及通信相关的程序库，无GUI工具。  
```
sudo apt-get install ros-kinetic-ros-base
```

+ 单个软件包安装: 你也可以安装某个指定的ROS软件包（使用软件包名称替换掉下面的PACKAGE）:  
```
sudo apt-get install ros-kinetic-PACKAGE
```
例如：
```
    sudo apt-get install ros-kinetic-slam-gmapping
```

要查找可用软件包，请运行：  
```
apt-cache search ros-kinetic`
```

## 2.5初始化 rosdep
```
sudo rosdep init
rosdep update
```
