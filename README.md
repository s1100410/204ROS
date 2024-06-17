# 204ROS
ROS期末專案(根據顏色進行自動導航的差速小車)，需要下載3個開源package才能使用(因launch檔有利用到)。  
準備工作：  
1. robot_navigation下載方式如下：  
  $cd ~/catkin_ws/src/  
  $git clone https://gitee.com/bingda-robot/robot_navigation.git  
  $cd ~/catkin_ws/  
  $catkin_make    
  $sudo apt-get install ros-$ROS_DISTRO-amcl ros-$ROS_DISTRO-move-base ros-$ROS_DISTRO-slam-gmapping ros-$ROS_DISTRO-slam-karto ros-$ROS_DISTRO-dwa-local-planner ros-$ROS_DISTRO-teb-local-planner ros-$ROS_DISTRO-map-server ros-$ROS_DISTRO-hector-slam*  
  $echo "export BASE_TYPE=NanoRobot" >> ~/.bashrc  
  $source  ~/.bashrc  

2. waterplus_map_tools下載方式如下：  
  $cd ~/catkin_ws/src/  
  $git clone https://github.com/6-robot/waterplus_map_tools.git  
  $cd waterplus_map_tools/scripts/  
  $./install_for_noetic.sh  
  $cd ~/catkin_ws/    
  $catkin_make  
4. $cd ~/catkin_ws/src/
   $git clone https://gitee.com/bingda-robot/bingda_tutorials.git  
   $cd ~/catkin_ws/    
   $catkin_make   
5. 將waypoint/waypoints.xml檔案的路徑存到"Z:\home\你的使用者名稱\waypoints.xml"，這樣用後續的rosFinalNav.launch才能抓到waypoints  
6. 執行根據顏色進行自動導航的差速小車：  
  $ roslaunch myrobot_1100410_description gazebo.launch (用來啟動差速小車及gazebo環境)  
  $ roslaunch myrobot_1100410_description rosFinalNav.launch (用來啟動rviz以及導航相關package，如map_server、amcl...)  
  $ rosrun myrobot_1100410_description rosNav.py (用來根據顏色進行自動導航)  
