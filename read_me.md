#Create a URDF pack based on SW

In this experiment, a URDF package is made. The robot used in this experiment is ABB-460 , a Four-Joints manipulator.
The download model：
![avatar](pic/sw2urdf/001.PNG)

#
#
Sldprt is a part of solidworks. We build a new assembly and then put scattered parts into the assembly to reassemble. But it's important to note that we must determine the coordinate system before reassembling.
![avatar](pic/sw2urdf/002.png)
#
#
The coordinate system in SolidWorks is left-handed, and the axis Y is upward.
![avatar](pic/sw2urdf/003.png)
#
#
However,the rendering coordinate system in Rviz is right-handed, and the axis Z is upward. 
![avatar](pic/sw2urdf/004.png)
#
#
The coordinate system of SW and rviz corresponds. The Y axis of SW is equal to the Z axis of rviz, so we must pay attention to it while reassembling. Select the base of the robot, move it to the origin of the world coordinate system before reassembling.
![avatar](pic/sw2urdf/005.png)
#
#
export URDF package:
![avatar](pic/sw2urdf/006.png)
#
#
install the plugin - sw2urdfSetup(download from wiki)
![avatar](pic/sw2urdf/007.PNG)
#
#
Then create the reference coordinate system and the rotating axis：
![avatar](pic/sw2urdf/008.png)
![avatar](pic/sw2urdf/009.png)
#
#
export：
![avatar](pic/sw2urdf/010.png)
![avatar](pic/sw2urdf/011.png)
![avatar](pic/sw2urdf/012.png)
![avatar](pic/sw2urdf/013.png)
![avatar](pic/sw2urdf/014.png)
![avatar](pic/sw2urdf/015.png)
![avatar](pic/sw2urdf/016.png)
#
#
change the parameter：
![avatar](pic/sw2urdf/017.png)
![avatar](pic/sw2urdf/018.png)
#
#
view the robot
catkin_make in you workspace：
roslaunch [your_package] display.lauch
change the item "fixedframe"
click the button "add" add a robot model:
![avatar](pic/sw2urdf/019.png)