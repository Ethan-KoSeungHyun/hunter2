# hunter2
Hunter2 Gazebo with GPS, IMU, Camera, Lidar (Ouster 64ch)





```bash
sudo apt-get install ros-noetic-ros-control -y
sudo apt-get install ros-noetic-ros-controllers -y
sudo apt-get install ros-noetic-gazebo-ros -y
sudo apt-get install ros-noetic-gazebo-ros-control -y
sudo apt-get install ros-noetic-joint-state-publisher-gui -y
sudo apt-get install ros-noetic-rqt-robot-steering -y
sudo apt-get install ros-noetic-hector-gazebo-plugins -y
```

```bash
mkdir hunter_ws
cd hunter_ws
mkdir src

git clone https://github.com/Ethan-KoSeungHyun/hunter2.git
```
```bash
cd ~/hunter_ws
source /opt/ros/noetic/setup.bash
rosdep install --from-paths src --ignore-src -r -y
catkin_make
```

```bash
# Rviz
cd hunter_ws
source devel/setup.bash

roslaunch hunter2_base display_xacro.launch
```
![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d004d024-a483-42cc-9eff-ef41eed51838/Untitled.png)

```bash
# Gazebo
cd hunter_ws
source devel/setup.bash

roslaunch hunter2_gazebo hunter2_empty_world.launch
```
![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dd9913bd-d201-45f2-8445-1ed59307fcc5/Untitled.png)
```bash
# Final
cd hunter_ws
source devel/setup.bash

roslaunch hunter2_gazebo hunter2_OS.launch
```
![Screenshot from 2023-07-09 21-00-57.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e558fcd5-a76f-458c-a8d8-79eeed5cf4d0/Screenshot_from_2023-07-09_21-00-57.png)
