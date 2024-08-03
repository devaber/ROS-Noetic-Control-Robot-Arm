# ROS-Noetic-Control-Robot-Arm
controlling the robot arm on ros noetic using joint_state_publisher, moveit and kinematics
Starting off you have to prepare a work space on ros
<h4>Create and Setup Work Space Using Catkin </h4> <br>
1- "mkdir catkin_ws" <br>
this command will create a new directory (folder), where mkdir stands for (make directory) then <br>
you can name it as you like, in this case it's "catkin_ws", this is where all your work will be saved. <br>
2- '''cd catkin_ws/''' <br>
use this command to get into you work space, where cd stands for (change directory) followed by the directory name,<br>
this command is used to navigate through directories
3- '''mkdir src''' <br>
this command will create a new folder where all your source code files will be saved and organized <br>
4- '''catkin_make''' <br>
this command will build your catkin work space, you might need to install catkin first so use this command <br>
'sudo apt install catkin' <br>
5- '''source devel/setup.bash''' <br>
this command will setup all the enviroment's variables, packages and everything you built using 'catkin_make' <br>
6- '''gedit ~/.bashrc''' <br>
you might need to install gedit first, so after installation is done, use this command to get into your bashrc file go to <br>
the bottom of this file, after last line add these 2 line: <br>
1- '''source /opt/ros/noetic/setup.bash''' <br>
if it is already writting then just write the next line <br>
2- '''source ~/catkin_ws/devel_setup.bash''' <br>
so hopfully now your enviroment is ready to start! <br>
<h4>Git and Git Clone</h4> <br>
1- '''scd src''' <br>
2- '''sudo apt install git''' <br>
this will install git <br>
3- '''git clone https://github.com/smart-methods/arduino_robot_arm''' <br>
in this command 'git clone' will copy an entire git repository from the provided link<br>
4- open new terminal window then get into your work space again 'cd catkin_ws/' <br>
5- '''rosdep install --from-paths src --ignore-src -r -y''' <br>
<h4>Installing</h4> <br>
1- '''sudo apt-get install ros-noetic-moveit''' <br>
2- '''sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui''' <br>
3- '''sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher''' <br>
4- '''sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control''' <br>
Finally <br>
5- '''catkin_make'''
<h4>Controlling The Robot Arm</h4> <br>
'''roslaunch robot_arm_pkg check_motors.launch''' <br>
this will launch RViz you can control the arm using the side panel <br>
'''roslaunch robot_arm_pkg check_motors_gazebo.launch''' <br>
this will launch Gazebo which is simulator for checking motors and components of the robot arm <br>
'''roslaunch moveit_pkg demo.launch''' <br>
here you can plan and control the robot arm motion
