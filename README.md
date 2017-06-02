# R4A ROS launchers


To use the package, first you must add it in a catkin workspace, build it and then source it:

```bash
cd ~/Desktop
mkdir -p r4a_launchers_ws/src
cd r4a_launchers_ws/src
catkin_init_workspace

git clone git@github.com:robotics-4-all/r4a_ros_launchers.git
cd ../
catkin_make

source devel/setup.bash
```

Available launchers:

- ```roslaunch r4a_launchers usb_cam.launch```: Launches a USB camera node and the image view window.


Notes to use Turtlebot:
- To connect: ```ssh r4a@192.168.2.240```. Ask for password!
- To connect to the Turtlebots ROS graph:
  - ```export ROS_MASTER_URI=http://192.168.2.240:11311```
  - ```export ROS_IP=localhost```
