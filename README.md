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

```bash
# Gazebo
cd hunter_ws
source devel/setup.bash

roslaunch hunter2_gazebo hunter2_empty_world.launch
```

```bash
# Final
cd hunter_ws
source devel/setup.bash

roslaunch hunter2_gazebo hunter2_OS.launch
```
