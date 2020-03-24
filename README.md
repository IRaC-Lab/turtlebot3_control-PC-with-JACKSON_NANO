# turtlebot3_remote_control
Controlling a turtlebot via other input.
-----------------------------------------------------------------------------------------------------
Overview
This is a part of the project to control Turtlebot3 via ROS Melodic.

First, install arduino IDE

Second, Setting arduino IDE

  1. In arduino IDE File -> Preferences ->Additional Boards Manager URLs
      typed "https://raw.githubusercontent.com/ROBOTIS-GIT/OpenCR/master/arduino/opencr_release/package_opencr_index.json
      
  2. In arduino IDE Tools -> Board: ~ ->Boards Manager... -> install "OpenCR by ROBOTIS"

  3. In arduino IDE Tools -> Board: ~ -> select "OpenCRBoard"

  4.In arduino IDE Tools -> Port: ~ -> Select Connected serial port

  5. Check firmware update 

Third, Download turtlebot3 burger firmware

   1.In arduino IDE File -> Examples -> turtlebot3 ->turtlebot3_burger -> turtlebot3_core

   2.click Upload button

Fourth, Installation of Turtlebot 3 Development Environment

Please refer to this site.
http://emanual.robotis.com/docs/en/platform/turtlebot3/ros2_setup/#hardware-setup

----------------------------------------------------------------------------------------------------

## How to control turtlebot3 speed?

directory: HOME -> catkin_ws -> src -> turtlebot3 -> turtlebot3_teleop -> nodes ->turtlelbot3_teleop_key

Change a value of LIN_VEL_STEP_SIZE and ANG_VEL_STEP_SIZE

## How we can change turtlebot3 control button?

directory: HOME -> catkin_ws -> src -> turtlebot3 -> turtlebot3_teleop -> nodes ->turtlelbot3_teleop_key

Change a value of key

-----------------------------------------------------------------------------------------------------

## How we can connect between PCs through ROS?

When we connect between PCs, we can't use 2 roscore. So we have to change value of ROS_MASTER_URI

directory of ROS_MASTER_URI : In terminal typed"gedit ~/.bashrc" -> Change value of ROS_MASTER_URI

In export ROS_HOSTNAME, we typed Enter the ip address of the device.

In export ROS_MASTER_URI, we typed the remotePC IP address.

example.
if remotePC IP address is xxx.xxx.x.xxx and turtlebot3 IP address is yyy.yyy.y.yyy,

In remotePC /.bashrc file, export ROS_HOSTNAME=xxx.xxx.x.xxx, export ROS_MASTER_URI=http://${ROS_HOSTNAME}:11311

In turtlebot3 /.bashrc file,  export ROS_HOSTNAME=yyy,yyy,y,yyy, export ROS_MASTER_URI=http://xxx.xxx.x.xxx:11311

-----------------------------------------------------------------------------------------------------

## How we can run this file?

Insturction 

1.roscore (remote PC)

2.roslaunch turtlebot3_bringup turtlebot3_robot.launch --screen (turtlebot3)

2.roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch --screen (remote PC)

-----------------------------------------------------------------------------------------------------

## How we can test this file without turtlebot3

Insturction 

1.roscore (remote PC)

2.roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch --screen (remote PC)

3.roslaunch turtlebot3_fake turtlebot3_fake.launch (remote PC)

-----------------------------------------------------------------------------------------------------
## Requirements

turtlebot3 burger

ROS Melodic

remote PC
