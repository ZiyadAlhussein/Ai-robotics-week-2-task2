# Ai-robotics-week-3-task2

**Task 1: Installing Arduino and Robotic arm packages in Ubunto 16.04**  

Follow through weeb 2 guide to install ubunto 16.04 with ROS in virtual machine:

(https://github.com/ZiyadAlhussein/Ai-robotics-week-2-tasks)

**1. Install Arduino in ubunto 16.04**

1) Download Arduino IDE for linux 64 bit: https://www.arduino.cc/en/software

![image](https://user-images.githubusercontent.com/108147030/181032737-79f7367c-2848-4251-8ed1-bc0448e5cef6.png)

2) go to the Files > downloads > right click on the comressed file and then click on extract here

![image](https://user-images.githubusercontent.com/108147030/181033692-781643a5-d82b-4d27-9ea8-cf9b90e6cb01.png)

3) go to the arduino file then right click > open in terminal:

![image](https://user-images.githubusercontent.com/108147030/181034084-6846aca4-c8c0-4f6a-99ae-eec344e27e5f.png)

4) type the following command to install Arduino:

```ruby
sudo ./installl.sh
```
**2. Running Robotic arm packages through ROS:**

1) Go to Terminal and run the following commands: 

```ruby
i. mkdir -p ~/catkin_ws/src

ii. cd ~/catkin_ws/

iii. catkin_make

iv. cd ~/catkin_ws/src

v. git clone https://github.com/smart-methods/arduino_robot_arm.git 

vi. cd ~/catkin_ws

vii. rosdep install --from-paths src --ignore-src -r -y

viii. sudo apt-get install ros-kinetic-moveit

ix. sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

x. sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

xi. sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control

xii. sudo nano ~/.bashrc

xiii. at the end of the (bashrc) file add the follwing line (source /home/ziyad/catkin_ws/devel/setup.bash)
then ctrl + o then ctrl + x (note:use your device name instead of "ziyad")

xiv. source ~/.bashrc

xv. roslaunch robot_arm_pkg check_motors.launch
```

2) The following program should run as shown below:

![image](https://user-images.githubusercontent.com/108147030/181041252-e13eb7ba-c2d9-4004-94cd-76620bbe313a.png)

![image](https://user-images.githubusercontent.com/108147030/181040884-b88ca106-9c6b-4c1a-8688-111016257661.png)


