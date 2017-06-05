# R4A ROS launchers


To use the package, first you must add it in a catkin workspace, build it and then source it:

```bash
cd ~/Desktop
mkdir -p r4a_launchers_ws/src
cd r4a_launchers_ws/src
catkin_init_workspace

git clone https://github.com/robotics-4-all/r4a_ros_launchers.git
cd ../
catkin_make

source devel/setup.bash
```

Available launchers:

- ```roslaunch turtlebot_bringup minimal.launch```: Bringsup Turtlebot.
- ```roslaunch r4a_launchers usb_cam.launch```: Launches a USB camera node and the image view window. This wont work with ssh since it raises a window.
- ```roslaunch openni2_launch openni2.launch```: Launches the driver for Asus Xtion.
- ```roslaunch r4a_launchers rplidar_standalone.launch```: Launches only the RPLidar. If you want to see the laser scan:
  - ```roslaunch r4a_launchers rplidar_standalone_rviz.launch```
- ```roslaunch r4a_launchers gmapping_turtlebot.launch```: Launches everything needed to execute GMapping in turtlebot (gmapping, turtlebot_bringup, rplidar and a static tf transform from base_link to laser)
- ```roslaunch r4a_launchers cartographer_turtlebot.launch```: Launches the cartographer slam, using the cartographer_turtlebot package, turtlebot_bringup, rplidar and a static tf transform.
- ```roslaunch kobuki_keyop keyop.launch```: Must be executed __after__ the turtlebot_bringup launcher and offers robot motion by keyboard arrows.
- ```roslaunch r4a_launchers movebase_turtlebot.launch```: Executes move base for Turtlebot.


Notes to use Turtlebot:
- To connect: ```ssh r4a@192.168.2.240```. Ask for password!
- To connect to the Turtlebots ROS graph:
  - ```export ROS_MASTER_URI=http://192.168.2.240:11311```
  - ```export ROS_IP=localhost```
