# RoboND-Term1-P2-Go-Chase-It
Project 2 of Udacity Robotics Software Engineer Nanodegree Program
![Overview](/videos/Term1-Project2-Go-Chase-It-Demo.gif)  
## Overview  
[TODO]  
In this project you'll create your simulation world in Gazebo for all your upcoming projects in the [Udacity Robotics Software Engineer Nanodegree Program](https://www.udacity.com/course/robotics-software-engineer--nd209).  
1. Build a single floor wall structure using the **Building Editor** tool in Gazebo. Apply at least one feature, one color, and optionally one texture to your structure. Make sure there's enough space between the walls for a robot to navigate.  
2. Model any object of your choice using the **Model Editor** tool in Gazebo. Your model links should be connected with joints.  
3. Import your structure and two instances of your model inside an empty **Gazebo World**.  
4. Import at least one model from the **Gazebo online library** and implement it in your existing Gazebo world.  
5. Write a C++ **World Plugin** to interact with your world. Your code should display ¡°Welcome to ¡¯s World!¡± message as soon as you launch the Gazebo world file.  
## Prerequisites/Dependencies  
* Gazebo >= 7.0  
* ROS Kinetic  
* make >= 4.1(mac, linux), 3.81(Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools]((https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
## Setup Instructions (abbreviated)  
1. Meet the `Prerequisites/Dependencies`  
2. Open Ubuntu Bash and clone the project repository  
3. On the command line execute  
```bash
sudo apt-get update && sudo apt-get upgrade -y
```
4. Build and run your code.  
## Project Description  
[TODO]  
Directory Structure  
```
.Build-My-World                    # Build My World Project 
©À©¤©¤ model                          # Model files 
©¦   ©À©¤©¤ gokart
©¦   ©¦   ©À©¤©¤ model.config
©¦   ©¦   ©À©¤©¤ model.sdf
©¦   ©À©¤©¤ myfloorplan
©¦   ©¦   ©À©¤©¤ model.config
©¦   ©¦   ©À©¤©¤ model.sdf
©¦   ©À©¤©¤ robot
©¦   ©¦   ©À©¤©¤ model.config
©¦   ©¦   ©À©¤©¤ model.sdf
©À©¤©¤ script                         # Gazebo World plugin C++ script      
©¦   ©À©¤©¤ welcome.cpp
©À©¤©¤ world                          # Gazebo main World containing models 
©¦   ©À©¤©¤ myoffice.world
©À©¤©¤ CMakeLists.txt                 # Link libraries 
©¸©¤©¤   
```
- [myoffice.world](/world/myoffice.world): Gazebo world file that includes the models.  
- [myfloorplan](/model/myfloorplan): A single floor structure designed in the Building Editor tool of Gazebo.  
- [gokart](/model/gokart): A go kart designed in the Model Editor tool of Gazebo.  
- [robot](/model/robot): A robot designed in the Model Editor tool of Gazebo.  
- [welcome.cpp](/script/welcome.cpp): Gazebo world plugin C++ script.  
- [Overview.png](/screenshots/Overview.png): A screenshot of the final result.  
- [CMakeLists.txt](CMakeLists.txt): File to link the C++ code to libraries.  
## Run the project  
[TODO]  
* Clone this repository
* Open the repository and make  
```
cd /home/workspace/RoboND-Term1-P2-Go-Chase-It/catkin_ws/
catkin_make
```
* Launch my_robot/my_gokart in Gazebo to load both the world and plugins  
```
roslaunch my_robot world.launch
```  
or  
```
roslaunch my_gokart world.launch
```  
* Launch ball_chaser and process_image node  
```
cd /home/workspace/RoboND-Term1-P2-Go-Chase-It/catkin_ws/
source devel/setup.bash
roslaunch ball_chaser ball_chaser.launch
```  
* Visualize  
```
cd /home/workspace/RoboND-Term1-P2-Go-Chase-It/catkin_ws/
source devel/setup.bash
rosrun rqt_image_view rqt_image_view  
```  

## Tips  
1. It's recommended to update and upgrade your environment before running the code.  
```bash
sudo apt-get update && sudo apt-get upgrade -y
```

## Code Style

Please (do your best to) stick to [Google's C++ style guide](https://google.github.io/styleguide/cppguide.html).

## Project Rubric  
### 1. Basic Requirements  
#### 1.1 Does the submission include the my_robot and the ball_chaser ROS packages?  
Yes, it does.  
### 1.2 Do these packages follow the directory structure detailed in the project description section?
Yes, it does.  
### 2. Robot Design
#### 2.1 Does the submission include a design for a differential drive robot, using the Unified Robot Description Format?  
Yes, it does.  
### 3. Gazebo World  
#### 3.1 Does the my_robot ROS package contain the Gazebo world?  
Yes, it does.  
### 4. Ball Chasing  
#### 4.1 Does the ball_chaser ROS package contain two C++ ROS nodes to interact with the robot and make it chase a white-colored ball?  
Yes, it does.  
### 5. Launch Files  
#### 5.1 Does the submission include world.launch and ball_chaser.launch files that launch all the nodes in this project?  
Yes, it does.  