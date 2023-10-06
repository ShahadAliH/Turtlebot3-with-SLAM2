# Turtlebot3-with-SLAM2
# Execute SLAM
In this case, we use gmapping that is general slam package.

File> New Tap
```
$cd catkin_ws
$source devel/setup.bash
$export TURTLEBOT3_MODEL=waffle_pi
$roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
![ROS](https://github.com/ShahadAliH/Turtlebot3-with-SLAM/assets/145300172/c9c28222-d247-4a30-bed7-c3abcdb1f449)
# Execute keypad
File> New Tap
```
$cd catkin_ws
$source devel/setup.bash
$export TURTLEBOT3_MODEL=waffle_pi
$roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
# Map output
File> New Tap
```
$cd catkin_ws
$source devel/setup.bash
$export TURTLEBOT3_MODEL=waffle_pi
$rosrun map_server map_saver -f ~/map
```
out and close terminal ( Execute keypad ) and ( Execute SLAM ).
# Activate Gazebo
```
$cd catkin_ws
$source devel/setup.bash
$export TURTLEBOT3_MODEL=waffle_pi
$roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
```
$cd catkin_ws
$source devel/setup.bash
$export TURTLEBOT3_MODEL=waffle_pi
$roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```
![ROS222](https://github.com/ShahadAliH/Turtlebot3-with-SLAM/assets/145300172/6d3c4e46-7f43-46f6-96d7-28d5ee05909d)
