### 1. What voltage needs to be supplied to the power jack? Is the NUC power supply sifficient to power the whole system?
### 2. What is the current draw of the whole system? / OR what capacity and specs for batteries di you use?  
### 3. Torso control board, which position for the key is "on"  
### 4. What voltage is requires for the torso control board? Is the USB conenction sufficient, or does it require power from the jack in addition?
### 5. Where would I find the schematics for the Torso control board (and really every other board designed by Callum?)  
### 6. What do you think will be the biggest issue with updating to latest version (distro) of ROS?  


- DJ Jack is the correct voltage, but will need more current draw 
- MARVIN has no voltage monitoring capability 
- Power board, all toggle swicthes   
- PCB schematics  
- RMP may not be supported, kinect drivers may not work and switching from python 2 to python 3 (especially print functions, which will need brackest around teh content of teh print). The kinect will be the most annoying thing. Look into getting a package mabager for C++ and Python.  
Ignore everything else, just work on the torso  
Then the next thing will be the torso animator, written in C++ as a ROS node.  
