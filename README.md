# SCARA Robot Control in ROS and Gazebo

## Project Overview

This project involves the development and control of a SCARA robot within the ROS and Gazebo simulation environment. The project is split into two main parts: configuring the robot in ROS/Gazebo and implementing control algorithms for its joints.

## Part 1: Robot Configuration

- Developed a SCARA robot in ROS and Gazebo, focusing on the configuration of joint types and link dimensions.
- Utilized cylinders to represent the robot's links for simplicity in visualization.

## Part 2: Robot Control

- Implemented a position controller for the prismatic joint of the SCARA robot.
- Designed a PD controller with tuned parameters for effective joint position control.
- Created a service client environment in ROS to command desired joint positions and observe the robot's response.
- Data on the robot's joint positions were recorded and analyzed, with results plotted in MATLAB for performance evaluation.

## How to Run

1. Launch Gazebo with the SCARA robot:
`roslaunch rrp_gazebo gazebo.launch`
2. Launch the position controller:
`roslaunch rrp_control rrp_effort_control.launch`
4. Execute the position control script:
`rosrun rrp_control rrp_pos_controller.py`
5. To set the desired joint position, use:
`rosservice call /set_joint_position "position: 0.2"`

## Results
![Screenshot 2024-03-09 at 7 40 18 PM](https://github.com/shreyas-chigurupati07/SCARA-robot/assets/84034817/1a9ce983-67a4-4a28-9461-d6852210eb19)
![Screenshot 2024-03-09 at 7 40 28 PM](https://github.com/shreyas-chigurupati07/SCARA-robot/assets/84034817/1af2b1b6-b331-4bad-9d4c-1af48fe5d73e)
## Dependencies

- ROS
- Gazebo
- MATLAB (for data analysis and plotting)

