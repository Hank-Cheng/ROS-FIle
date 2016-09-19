# ROS-File

Used ROS: indigo

Used Arduino 1.0.6

OS: LUNIX 14.04LTS


step 1
download arduino rosserial
$sudo apt-get install ros-indogo-rosserial ros-indigo-rosserial-arduino

Insert the library to arduino 

$cd ~/sketchbook/libraries

$rosrun rosserial_arduino make_libraries.py ~/sketchbook/libraries

then you can find 

Sketch->library->ros_lib

=====commute to arduino ======

//new

$roscore

//new 

$rosrun rosserial_python serial.node.py _port:=/dev/ [USB PORT NAME]

if you got error, change the permission

$sudo chmod 777 /dev/[USB PORT]

//new

send  message to arduino 

$rostopic pub /led std_msgs/Bool true

$rostopic pub /led std_msgs/Bool false

Chinses-中文註解-
這篇是在說明如何運用ROS來連接ARDUINO，將Arduino 連接上ROS node上面

