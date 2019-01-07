
kinect head pose estimation with OSC support

Includes standalone version and pix_head_pose_estimation Pure Data/Gem external.

Standaloe works with libfreenect, OpenNI or Microsoft Kinect SDK (Windows only)

based on 
Real Time Head Pose Estimation from Consumer Depth Cameras 
by Gabriele Fanelli
http://www.vision.ee.ethz.ch/~gfanelli/head_pose/head_forest.html

======================================

Application that detects head position from a depth image provided by
Kinect Sensor in x,y,z and Euler Angles (pitch, yaw, roll) 
from multiple persons.

Application sends data as OSC Message in the format:

/head_pose [User_ID] [x] [y] [z] [pitch] [yaw] [roll]

all arguments are float, angles in degree, User_ID starting at zero.

Usage:
* #.../head_pose_estimation> ./head_pose_estimation_demo config.txt <show visual 0 or 1> <send osc 0 or 1> <osc-ip> <osc-port>

example how to not show visualization and use custom ip and port for sending OSC Messages:

./head_pose_estimation_demo config.txt 0 1 192.168.0.1 8000

Default IP/Port: 127.0.0.1:7120


* you can find an example puredata/GEM patch in the folder pd	
to visualize the headtracking.

(C) 2011/2012 by Matthias Kronlachner
__________________________________________________________

Arch Linux
-----------------

* sudo pacman -S cmake opencv freeglut

* pacaur -S libfreenect openni liblo

* cd demo/
*	#.../head_pose_estimation/demo> cmake CMakeLists.txt
*	#.../head_pose_estimation/demo> make


*	#.../head_pose_estimation> ./head_pose_estimation_demo config.txt


questions: m.kronlachner@gmail.com


