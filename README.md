Setup procedures before you run any ROS packages:

1) 'source /opt/ros/melodic/setup.bash' from your ROS master
2) 'source ./catkin_ws/devel/setup.bash' from your ROS master
3) 'export ROS_MASTER_URI=[insert MASTER URI]' on your laptop AND Pi
4) 'export ROS_IP=[insert local IP]' on your laptop AND Pi
5) Run 'roscore' from your ROS master device

Running LiDAR & SLAM:
1) Start LiDAR data reading: Execute 'roslaunch rplidar_ros rplidar.launch' from your Pi
2) Start Hector SLAM & rviz: Execute 'roslaunch rplidar_ros view_slam.launch' from your laptop
3) Show your Alex on the rviz map: 'Add' -> 'rviz -> TF' -> 'OK', then under 'Displays' -> 'TF' -> 'Frames' deselect 'base_link', 'map' and 'scanmatcher_frame'. The green line is your Alex, and the red arrow indicate which direction the LiDAR is facing

In this repo:
1) hector_slam: Compiled for amd64
2) rplidar_ros: Compiled for amd64
