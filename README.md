# ROS2 Reference for Humble Hawksbill Distro

## Clone ROS2 Training Repository 
```
git clone https://x-token-auth:ATCTT3xFfGN0Ei77SyYV1u0xnKHgDbi7oHsVr-0lGiWZxW3yKX90ylwDssZrtC2S_tKlzIBkr686dGB9XlEeEdhoxh4uqXTyMCdPM2NmM0SavJz30TICaMioP2CUmvB3kxTLdfA-82uedoUrXjonurSCIeGsoBa2UDKt_APB3QqpTtKkge7rpPY=1E7A68CF@bitbucket.org/team_ntu_arc/training_dlsu.git
```
## Update (always do this before installing in ubuntu)
```
sudo apt update
```

## Install terminator for ubuntu terminal
```
sudo apt-get install terminator
```

## Install git
```
sudo apt install git-all
```

## Configure Git information
```
git config --global user.name "[your name]"
git config --global user.email "[your email]"
```

## ROS2 Create Package 
```
ros2 pkg create [package-name] --build-type ament_python --dependencies rcply std_msgs geometry_msgs/msg/Twist
```

## ROS2 Build Package
```
colcon build --symlink-install
```

## Run Transform 
```
ros2 run tf2_ros static_transform_publisher 0.0 0 0.3 0 0 0 tool0 camera_link
ros2 run tf2_ros tf2_echo base_link tool0
```

## Install UR library 
```
sudo apt-get install ros-humble-ur-client-library
sudo apt-get install ros-humble-ur
```

## Install Transform packages
```
sudo apt-get isntall ros-humble-tf-transformations
sudo apt-get install ros-humble-tf2-ros
```

## Launch UR and Moveit(?)
```
ros2 launch ur_description view_ur.launch.py ur_type:=ur10
ros2 launch ur_moveit_config ur_moveit.launch.py ur_type:=ur10
ros2 launch ur_robot_driver ur_control.launch.py ur_type:=ur10 robot_ip:=192.168.11.100 launch_rviz:=false use_fake_hardware:=true
```

## Install gazebo 
```
sudo apt install ros-humble-gazebo-*
```

## Install example libraries
```
sudo apt-get install ros-humble-turtlebot3-msgs ros-humble-cartographer ros-humble-cartographer-ros ros-humble-navigation2
```

## Install python extensions
```
sudo apt install python3-colcon-common-extensions
```

## Other training libraries
```
git clone -b humble https://github.com/ROBOTIS-GIT/DynamixelSDK.git
git clone -b humble https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
git clone -b humble https://github.com/ROBOTIS-GIT/turtlebot3.git
git clone -b humble https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
```




