# Extend Kalman Filter Project
here you will find ROS project that apply EKF fusing LIDAR and IMU readings to localize the robot pose by predicting its path and compare it with the unfiltered and un fused data.  

# Prerequisites
you should have the following list installed

* ROS melodic 
* GAZEBO 
* RViz
* catkin pakage

# Install and Launch
 
``` 
first download the project
   
    $ git clone https://github.com/Abdelrahman-Hanafy/EKF_Lab.git

then **BUILD** the project

    $ cd [path where you cloned]/EKF_Lab
    $ catkin_make 

TO launch using roslaunch

    $roslaunch main main.launch 
```

# Project Dirs Structure

```
.EKF_Lab                                        # Project workspace
├── media                                       # media folder for the project 
│   ├── Screencast from 06-09-20 00:18:16.mp4
│   ├── Screenshot from 2020-09-05 23-02-07.png
│   └── Screenshot from 2020-09-06 00-15-18.png
├── README.md
└── src
    ├── CMakeLists.txt -> /opt/ros/melodic/share/catkin/cmake/toplevel.cmake 
    ├── main                                    # main package to launch the prject
    │   ├── CMakeLists.txt                      # compiler instructions
    │   ├── configration                        # config folders for configration files
    │   │   └── rqt_multiplot.xml
    │   ├── launch                              # launch folder for launch files
    │   │   ├── main.launch
    │   │   └── rviz_launch.launch
    │   ├── package.xml
    │   └── rviz                                # rviz folder for rviz configration
    │       └── ekf.rviz
    ├── my_robot                                # my_robot package 
    │   ├── CMakeLists.txt                      # compiler instructions
    │   ├── launch                              # launch folder for launch files
    │   │   ├── robot_description.launch
    │   │   └── world.launch
    │   ├── meshes                              # meshes folder for sensors
    │   │   └── hokuyo.dae
    │   ├── package.xml
    │   ├── urdf                                # urdf folder for xarco files
    │   │   ├── my_robot.gazebo
    │   │   └── my_robot.xacro
    │   └── worlds                              # world folder for world files
    │       ├── empty.world
    │       └── world.world
    ├── odom_to_trajectory                      # path drawing pkg
    └── robot_pose_ekf                          # Extended Kanon Filter pkg


```
