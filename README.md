# Task2-Robotics-and-AI
This task contains the steps of motion trajectories execution for a robot arm in simulation.
## Steps:
1- Install ROS.

2- Chage the directory to catkin/src:
```
$ cd ~/catkin_ws/src
```
3- Install git:
```
$ sudo apt install git
```
4- clone the repository:
```
$ git clone https://github.com/smart-methods/arduino_robot_arm 
```
5- Install all the dependencies 
```
$ cd ~/catkin_ws
$ rosdep install --from-paths src --ignore-src -r -y
$ sudo apt-get install ros-noetic-moveit
$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
6- Compile the package
```
$ catkin_make
```
7- Controlling the robot arm by joint_state_publisher
```
$ roslaunch robot_arm_pkg check_motors.launch
```
8- Controlling the motors joint_state_publisher
```
$ rqt_graph
$ rostopic echo /joint_states
```
