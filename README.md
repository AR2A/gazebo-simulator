# gazebo-simulator
## Overview
This repository contains all files for the rescue robot gazebo simulator.

## Preparation
In order to use the _AR2A_ robot inside Gazebo, create following three packages
inside your _catkin workspace_:

* ar2a_control
* ar2a_description
* ar2a_gazebo

and copy the content from the repository into these folders.

Make sure following ROS packages are installed:

* ros-indigo-effort_controllers
* ros-indigo-joint_state_controller

## Starting the simulation
To start the simulation, run:

 * roslaunch ar2a_gazebo ar2a.launch

This opens Gazebo as well as Rviz, in order to visualize what AR2A robot is seeing 
through it's sensors.

To drive around, either start the turtle teleop node:

* rosrun turtlesim turtle_teleop_key /turtle1/cmd_vel:=/AR2A/cmd_vel

or the AR2A _robotcontrol_ node:

* rosrun robotcontrol robotcontrol_node /RobotControl:=/AR2A/cmd_vel
