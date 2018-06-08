From version 2, this node aims to play the whole kitti data into ROS (Color/Grayscale images, Velodyne scan as PCL, sensor_msgs/Imu Message, GPS as sensor_msgs/NavSatFix Message). 

http://www.ira.disco.unimib.it/kitti_player
https://github.com/iralabdisco/kitti_player

=========

Kitti_player, a player for KITTI raw datasets
Datasets can be downloaded from: http://www.cvlibs.net/datasets/kitti/raw_data.php

Allowed options:          
help     __      h  __  help message    
directory   __   d  __  *required* - path to the kitti dataset Directory    
frequency   __   f  __  set replay Frequency    
all       __     a  __  replay All data     
velodyne   __    v  __  replay Velodyne data    
gps    __        g __   replay Gps data    
imu     __       i __   replay Imu data    
grayscale    __  G __   replay Stereo Grayscale images    
color  __        C __   replay Stereo Color images    
viewer  __       V  __  enable image viewer    
timestamps  __   T __   use KITTI timestamps    
stereoDisp  __   s  __  use pre-calculated disparities    
viewDisp  __     D  __  view loaded disparity images    
frame    __      F __   start playing at frame...    
gpsPoints  __    p __   publish GPS/RTK markers to RVIZ, having reference frame as <reference_frame> [example: -p map]    
synchMode  __    S  __  Enable Synch mode (wait for signal to load next frame [std_msgs/Bool "data: true"]    
    
kitti_player needs a directory tree like the following:
└── 2011_09_26_drive_0001_sync
    ├── image_00              
    │   └── data              
    │   └ timestamps.txt      
    ├── image_01              
    │   └── data              
    │   └ timestamps.txt      
    ├── image_02              
    │   └── data              
    │   └ timestamps.txt      
    ├── image_03              
    │   └── data              
    │   └ timestamps.txt      
    ├── oxts                  
    │   └── data              
    │   └ timestamps.txt      
    ├── velodyne_points       
    │   └── data              
    │     └ timestamps.txt    
    └── calib_cam_to_cam.txt  

