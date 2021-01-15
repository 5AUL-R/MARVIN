# Update documentation  
This readme file will serve as a centralised location for all import changes across ROS distros between Indigo to Melodic.  
Additionally, this readme will serve as a log to all changes made to software - for the purposes of documentation and future bug fixing.  

## Notes for software migration from Callum
1. torso_control - all in python shouldn't be too hard - get it to the point you can send ROS messages manually and see the torso change as a result.
2. segway_rmp - get the latest version from the ros wiki, hope it is still supported.
3. torso_animator - in cpp, might be a bit more annoying, but this will let you request animations rather than just poses.
4. then worry about getting the existing sensors working, or consider replacing them with new ones that are easier to support.

## Package list 
Key:  
D = discontinued and / or unavailable  
A = active but not support for melodic  
AC = active and support for melodic  
### Rosserial [AC]
### map_server [AC]
### base_local_plannr [AC]
### move_base [AC]
### ROS GMapping package [AC]
### AMCL
### segway_rmp [D]



## ROS distro log  
### Indigo Igloo
### Jade Turtle 
### Kinetic Kame
### Lunar Loggerhead
### Melodic Morenia
