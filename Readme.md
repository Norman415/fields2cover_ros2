# Fields2Cover ROS2 RViz 可视化

本项目用于将 [Fields2Cover](https://github.com/Fields2Cover/Fields2Cover) 路径规划结果通过 ROS2 和 RViz2 进行可视化。

## 1. 环境要求

推荐环境：

- Ubuntu 20.04
- ROS2 Foxy
- C++17
- RViz2
- Fields2Cover

如果使用其他 ROS2 版本，请根据实际环境调整依赖包或者CmakeList.txt。

---

## 2. 安装 rviz_satellite

本项目的 RViz 可视化界面使用 `rviz_satellite` 显示卫星地图。

首先安装相关依赖：

cd ~/ros2_ws/src

git clone https://github.com/nobleo/rviz_satellite.git

cd ~/ros2_ws

rosdep install --from-paths src --ignore-src -r -y

colcon build --symlink-install --packages-select rviz_satellite


## 3. 运行
source /opt/ros/foxy/setup.zsh
source install/setup.zsh
ros2 run fields2cover_ros visualizer_node

## 4.可视化
source install/setup.zsh
ros2 launch fields2cover_ros view_field.launch
