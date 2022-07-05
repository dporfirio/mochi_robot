Mochi Robot

# Prerequisites

Beyond having a general familiarity with ROS and Ubuntu, the following are the hardware and software requirements that you will need to assemble the Mochi Robot:

## Hardware

The following hardware is used for this project:

- **Robot base**: iRobot Create2
- **LiDAR**: Slamtec RPLidar A1
- **Driver Computation**: Raspberry Pi 4 with Ubuntu 20
- **Battery Pack**: RPi UPSPack Standard V3P

In total, the hardware required for this project will cost a few hundred US dollars.

## Software (on the Raspberry Pi)

The following libraries must be installed on the Raspberry Pi:

- ROS Noetic (this guide assumes that you have created a workspace `~/catkin_ws`.

Run the following commands to install the required ROS packages:

```
cd ~/catkin_ws/src
git clone git@github.com:dporfirio/mochi_robot.git
git clone git@github.com:AutonomyLab/create_robot.git
git clone git@github.com:AutonomyLab/libcreate.git
git clone git@github.com:Slamtec/rplidar_ros.git
```

# Build and Run

```
# to build
cd ~/catkin_ws
catkin build
source devel

# to run
roslaunch mochi mochi.launch
```

# Troubleshooting

Make sure that you have input the RPLidar and the Create2 robot to the correct USB ports. I have RPLidar set to USB1 and the Create2 robot set to USB0.
