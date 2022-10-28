# ur5e_actual
ur5e_actual

### 1. Requirements
System: Ubuntu 18.04, Ubuntu 20.04   

ROS: Melodic, Noetic    
 
Moveit   

   

### 2. Other Dependencies
For some dependencies were missed for the project, please check the following instructions.
```
sudo apt-get install ros-melodic-moveit-visual-tools
sudo apt-get install ros-melodic-ros-controllers
sudo apt-get install ros-melodic-ur-client-library
sudo apt-get install ros-melodic-ur-msgs
```

**NOTE:**There might be more dependencies needed due to vairous reasons. If you found any, please let me know.(archer7wang@outlook.com)

### 3. Usage
Like ordinary ros projects, the simluation needs a clean workspace.
```
mkdir -p ur5e_actual_ws/src
cd src
git clone https://github.com/wangarcher/ur5e_actual.git
cd ..
catkin_make
source devel/setup.bash
``` 
##### 0. Power up the UR5e robot
Press the power bottom in the UR5e robot panel. And wait, then power on the robot by clicking the red icon in the left bottom.


##### 1. Initialization
To connect the UR5e robot with the PC. 
```
roslaunch ur_robot_driver ur5e_bringup_with_ip.launch
```

##### 2. Start the interface
To run the interface
```
roslaunch ur5e_move_group_interface run_arm.launch
```

##### 3. Plan
To run the project planning node
```
rosrun ur5e_plan project_plan
```
