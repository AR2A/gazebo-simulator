# gazebo-simulator
## Overview
This repository contains all files for the rescue robot gazebo simulator.

## Preparation
### Dependencies
Make sure following ROS packages are installed:

* ros-indigo-effort_controllers
* ros-indigo-joint_state_controller
* ros-indigo-hector-gazebo-plugins

```
sudo apt-get install ros-indigo-effort_controllers ros-indigo-joint_state_controller ros-indigo-hector-gazebo-plugins
```

### Clone
In order to use the _AR2A_ robot inside Gazebo, clone this repository and copy this three packages
inside your _catkin workspace_:

* ar2a_control
* ar2a_description
* ar2a_gazebo

```
git clone https://github.com/AR2A/gazebo-simulator.git
cp -av ./gazebo-simulator/ar2a* /your/catkin_workspace
```

## Starting the simulation
To start the simulation, run:

```
roslaunch ar2a_gazebo ar2a.launch
```

This opens Gazebo as well as Rviz, in order to visualize what AR2A robot is seeing 
through it's sensors.

### Gazebo Screenshot

<img style="float: middle;" src="https://github.com/AR2A/gazebo-simulator/blob/master/img/gazebo.png">

### Rviz Screenshot

<img style="float: middle;" src="https://github.com/AR2A/gazebo-simulator/blob/master/img/rviz.png">

To drive around, either start the turtle teleop node:

```
rosrun turtlesim turtle_teleop_key /turtle1/cmd_vel:=/cmd_vel
```

or the AR2A _robotcontrol_ node:

```
rosrun robotcontrol robotcontrol_node /RobotControl:=/cmd_vel
```
