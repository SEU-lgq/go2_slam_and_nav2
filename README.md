<<<<<<< HEAD
# Unitree Go2导航功能
本项目基于https://github.com/FishPlusDragon/unitree-go2-slam-toolbox项目的slam建图部分，完成了机器狗nav2部分代码的更新。
## 实现功能
1.在文件中添加机器狗模型
2.编写了nav2核心模块。包括AMCL定位，planner和controller模块
## 开发环境配置
该项目运行在Ubuntu22.04的ros2 humble上

参考宇树开发文档 
和b站赵虚左老师的课程 BV1vv5YzBEQH
## 依赖安装
```bash
sudo apt install -y \
  ros-humble-robot-localization \
  ros-humble-slam-toolbox \
  ros-humble-navigation2 \
  ros-humble-laser-geometry \
  ros-humble-message-filters \
  ros-humble-tf2-sensor-msgs \
  python3-colcon-common-extensions
```
## 快速开始
### 1.创建工作空间
```bash
mkdir -p go2_slam_and_nav2/src && cd go2_slam_and_nav2/src
```
### 2.克隆仓库
```bash
git@github.com:SEU-lgq/go2_slam_and_nav2.git
```
### 3.编译工作空间
```bash
cd .. && colcon build
```
### 4.启动
1.加载环境变量

```bash
source install/setup.bash
```
2.启动slam建图

```bash
ros2 launch go2_core go2_start.launch.py
```
打开新终端

3.保存建图
```bash
ros2 launch go2_navigation2 go2_save_map.launch.py
```
关闭原来的rviz2
4.启动导航功能
```bash
ros2 launch go2_navigation2 go2_nav2.launch.py
```
=======
基于https://github.com/FishPlusDragon/unitree-go2-slam-toolbox项目的slam建图部分，完成了机器狗nav2部分代码的更新。
>>>>>>> cd1934147ab57ff16b7e05772717667c6f9bb0d1
