1) Install Ubuntu-22.04 and ROS2 Humble before connecting realsense camera.

   If using WSL you may need to attach a usb device: https://learn.microsoft.com/en-us/windows/wsl/connect-usb#attach-a-usb-device



2) Install Intel Realsense ROS2 Wrapper for Ubuntu: https://github.com/IntelRealSense/realsense-ros/blob/ros2-master/README.md#installation-on-ubuntu

   For step 2 (install SDK), option 2 (debian packages) may be chosen.

   Alternatively, for step 2 (install SDK), you may follow option 1 especially if you want to test using "realsense-viewer": https://github.com/IntelRealSense/librealsense/blob/master/doc/distribution_linux.md#installing-the-packages

   (don't forget to upgrade the packages)

   For step 3 (ROS2 wrapper), option 1 (debian packages) may be chosen.



4) cd ~/ros2_ws/src

   git clone https://github.com/bjahoor/cam_package

   cd ~/ros2_ws

   source /opt/ros/humble/setup.bash

   colcon build --packages-select cam_package



6) sudo apt install ros-humble-image-transport ros-humble-image-transport-plugins



7) source install/setup.bash

   ros2 launch cam_package cam.launch.py
