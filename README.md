From version 2, this node aims to play the whole kitti data into ROS (Color/Grayscale images, Velodyne scan as PCL, sensor_msgs/Imu Message, GPS as sensor_msgs/NavSatFix Message). 

http://www.ira.disco.unimib.it/kitti_player
https://github.com/iralabdisco/kitti_player

=========

Kitti_player, a player for KITTI raw datasets     
Datasets can be downloaded from: http://www.cvlibs.net/datasets/kitti/raw_data.php     

Allowed options:      
help___________h____help message    
directory______d____*required* - path to the kitti dataset Directory    
frequency______f____set replay Frequency    
all____________a____replay All data    
velodyne_______v____replay Velodyne data    
gps____________g____replay Gps data    
imu____________i____replay Imu data     
grayscale______G____replay Stereo Grayscale images    
color__________C____replay Stereo Color images    
viewer_________V____enable image viewer    
timestamps_____T____use KITTI timestamps     
stereoDisp_____s____use pre-calculated disparities    
viewDisp_______D____view loaded disparity images     
frame__________F____start playing at frame...    
gpsPoints______p____publish GPS/RTK markers to RVIZ, having reference frame as <reference_frame> [example: -p map]    
synchMode______S____Enable Synch mode (wait for signal to load next frame [std_msgs/Bool "data: true"]    
     
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

