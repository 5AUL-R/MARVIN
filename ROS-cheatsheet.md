# ROS Cheat sheet
## Environment Variables
### ROS_PACKAGE_PATH
- Stored in the `~/.bashrc` file. Can be modified by running: `sudo nano ~/.bashrc`  (Although it's reccomended that you *really know what you're doing before trying this)  
- Can be checked in terminal by running `echo $ROS_PACKAGE_PATH` 
- Can be appeneded (added to) by running `ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:new/directories/you/want`  
  (**It's very important to note: you should never directly change the package path, rather you should appened another directory**)
