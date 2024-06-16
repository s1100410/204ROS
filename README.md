# 204ROS
ROS期末專案，需要下載兩個開源package才能使用(因launch檔有利用到)。

1.robot_navigation下載方式如下：
  cd ~/catkin_ws/src/
  git clone https://gitee.com/bingda-robot/robot_navigation.git
  cd ~/catkin_ws/
  catkin_make
  
  sudo apt-get install ros-$ROS_DISTRO-amcl ros-$ROS_DISTRO-move-base ros-$ROS_DISTRO-slam-gmapping ros-$ROS_DISTRO-slam-karto ros-$ROS_DISTRO-dwa-local-planner ros-$ROS_DISTRO-teb-local-planner ros-$ROS_DISTRO-map-server ros-$ROS_DISTRO-hector-slam*
  
  echo "export BASE_TYPE=NanoRobot" >> ~/.bashrc
  source  ~/.bashrc

2.waterplus_map_tools下載方式如下：
  cd ~/catkin_ws/src/
  git clone https://github.com/6-robot/waterplus_map_tools.git
  cd waterplus_map_tools/scripts/
  ./install_for_noetic.sh
  cd ~/catkin_ws/  
  catkin_make
