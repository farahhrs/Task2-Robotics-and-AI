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
![image](https://user-images.githubusercontent.com/67878227/181501406-bcc4c2ec-9b5a-4e81-a4fb-b79292c3f3ec.png)

8- Controlling the motors joint_state_publisher
```
$ rqt_graph
```
![image](https://user-images.githubusercontent.com/67878227/181501569-4898bd46-e5f7-429e-a645-eaed79013f64.png)

```
$ rostopic echo /joint_states
```
![image](https://user-images.githubusercontent.com/67878227/181501642-313bb5d6-9bc2-48dc-b593-1673b49b31bb.png)

## Arduino IDE installation on Ubunto steps:
1- Create new directory with the name "arduino":
```
$ mkdir arduino
```
2- Change the directory:
```
$ cd arduino/
```
3- Download Arduino IDE:
```
$ wget https://downloads.arduino.cc/arduino-1.8.15-linux64.tar.xz
```
4- Extract the tar.xz file:
```
$ tar -xvf ./arduino-1.8.15-linux64.tar.xz
```
5- Change the directory:
```
$ cd arduino-1.8.15/
```
6- Run the installed script:
```
$ sudo ./install.sh
```
Note: By default Arduino is installed to /usr/local/bin/arduino, you can find a new icon on the desktop and application list
