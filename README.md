# UR5_ROBOTIQ85_PICKNPLACE

NOTES:  
- There are issues documented about MoveIt! generated packages and gazebo about the controllers.  
- See the videos section for the solution.

<details open>
<summary> <b>Brief Review<b></summary>

This project includes all necessary files reproduce a simulation of the UR5 Robotic Manipulator and a RobotIQ85 2 DoF robotic ARM.  

At this point we only have the simulations of:
- Viewing the UR5 and gripper separately in rviz
- Viewing the UR5 and gripper as one in rviz
- Viewing the UR5 and gripper separately in gazebo
- Viewing the UR5 and gripper as one in gazebo
- Using the UR5 and gripper separately in rviz with MoveIt! rviz interface
- Using the UR5 and gripper as a standalone device in rviz with MoveIt! and check the execution in gazebo.

I based the structure of this repository using [Stanley Automation RobotIQ85](https://github.com/StanleyInnovation/robotiq_85_gripper.git) and [UR5 from ROS-Industrial](https://github.com/ros-industrial/universal_robot.git). 

Below an image example of the outcome after the command:

    roslaunch ur5_picknplace gripper_arm_rviz_MoveIt!_gazebo.launch world_name:='$(find ur5_picknplace)/worlds/ur5_floor_objects.world'

<p align="center">
<img src = "doc/imgs/ur5_robotiq85_world.PNG?raw=true" width="65%"/>
</p>

</details>

<details open>
<summary> <b>Using the ur5_robotiq85_picknplace package<b></summary>

- Create a ROS ros workspace and compile an empty package:
~~~
    cd ~
    mkdir -p catkin_ws/src
    cd catkin_ws
    catkin_make
~~~
- Open the `.bashrc` with nano:
~~~
    nano ~/.bashrc
~~~    
- Insert this line at the end of the `~/.bashrc` file for sourcing your workspace:
~~~
    source ~/catkin_ws/devel/setup.bash
~~~
- Clone this repo in the `~/catkin_ws/src` folder by typing:
~~~ 
    cd ~/catkin_ws/src
    git clone https://github.com/issaiass/ur5_robotiq85_picknplace --recursive
    git clone https://github.com/StanleyInnovation/robotiq_85_gripper
    git clone https://github.com/ros-industrial/universal_robot.git
    cd ..
~~~
- Go to the root folder `~/catkin_ws` and make the folder running `catkin_make` to ensure the application compiles.
- Now you can test in several ways the packages
- For viewing in rviz each element or the arm with the gripper, choose anyone of these launch files
~~~
    roslaunch ur5_picknplace view_arm.launch
    roslaunch ur5_picknplace vew_gripper.launch
    roslaunch ur5_picknplace vew_gripper_arm.launch    
~~~
- Visualizing in gazebo, choose anyone of these launch files 
~~~
    roslaunch ur5_picknplace spawn_arm.launch
    roslaunch ur5_picknplace spawn_gripper.launch
    roslaunch ur5_picknplace spawn_gripper_arm.launch    
~~~
- For just visualizing in gazebo and rviz simultaneously, choose anyone of these launch files
~~~
    roslaunch ur5_picknplace arm_gazebo_rviz.launch
    roslaunch ur5_picknplace gripper_gazebo_rviz.launch
    roslaunch ur5_picknplace gripper_arm_gazebo_rviz.launch
~~~
- For controlling using rviz MoveIt! and visualizing the movement in gazebo for the gripper and the arm
~~~
    roslaunch ur5_picknplace gripper_arm_rviz_MoveIt!_gazebo.launch
~~~


<details closed>
<summary> <b>Results<b></summary>

You could see the results on this youtube video.  

<p align="center">

No video will be posted until it works completely

</p>

</details>

<details open>
<summary> <b>Video Explanation<b></summary>

<p align="center">

Solution of the error of UR5 and RobotIQ Gripper with MoveIt! 2.0
Part 2/2 - UR5 RobotIQ Gripper MoveIt! 2.0 - Unable to identify any set of controllers that can..

[<img src= "https://img.youtube.com/vi/TcUmlq6eStg/0.jpg" />](https://youtu.be/TcUmlq6eStg)

Previous Videos

[Part 1/2 - UR5 RobotIQ Gripper MoveIt! 2.0 - Unable to identify any set of controllers that can...](https://youtu.be/lGJM86NhGGQ)

</p>

</details>

<details open>
<summary> <b>Issues<b></summary>

- demo_gazebo.launch executes correctly, but when you try to control the arm and gripper the execution fails.

</details>

<details open>
<summary> <b>Future Work<b></summary>
- :heavy_check_mark: Solved issue of the robotic arm not moving in gazebo
- :x: Finish the worlds

</details>

<details open>
<summary> <b>Contributing<b></summary>

Your contributions are always welcome! Please feel free to fork and modify the content but remember to finally do a pull request.

</details>

<details open>
<summary> :iphone: <b>Having Problems?<b></summary>

<p align = "center">

[<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/riawa)
[<img src="https://img.shields.io/badge/telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/>](https://t.me/issaiass)
[<img src="https://img.shields.io/badge/instagram-%23E4405F.svg?&style=for-the-badge&logo=instagram&logoColor=white">](https://www.instagram.com/daqsyspty/)
[<img src="https://img.shields.io/badge/twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white" />](https://twitter.com/daqsyspty) 
[<img src ="https://img.shields.io/badge/facebook-%233b5998.svg?&style=for-the-badge&logo=facebook&logoColor=white%22">](https://www.facebook.com/daqsyspty)
[<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/riawe)
[<img src="https://img.shields.io/badge/tiktok-%23000000.svg?&style=for-the-badge&logo=tiktok&logoColor=white" />](https://www.linkedin.com/in/riawe)
[<img src="https://img.shields.io/badge/whatsapp-%23075e54.svg?&style=for-the-badge&logo=whatsapp&logoColor=white" />](https://wa.me/50766168542?text=Hello%20Rangel)
[<img src="https://img.shields.io/badge/hotmail-%23ffbb00.svg?&style=for-the-badge&logo=hotmail&logoColor=white" />](mailto:issaiass@hotmail.com)
[<img src="https://img.shields.io/badge/gmail-%23D14836.svg?&style=for-the-badge&logo=gmail&logoColor=white" />](mailto:riawalles@gmail.com)

</p

</details>

<details open>
<summary> <b>License<b></summary>
<p align = "center">
<img src= "https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg" />
</p>
</details>