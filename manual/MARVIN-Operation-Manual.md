# MARVIN operation MANUAL  
Last edited 11/2/2021  

## Table of contents
## 1.0 Introduction  
Mobile Autonomous Robotic Vehicle for Indoor Navigation V2.0 or MARVIN (V2) for short is a Robot originally designed for use as a prototype security system by Dale Carnegie.  
His use as a research tool over time has shifted his uses from security to Human Robot Interaction.   
The most recent project he has been utilised for was Callum Robinson's Masters thesis. He modified MARVIN's hardware and software systems to suit his change into an HRI platform.

## 1.1 Prerequisite Knowledge
### 1.1.1 Linux and Command Line
This manual will assume you are reasonably familiar with navigating a Linux / Unix desktop environemnt and command terminal (specifically with BASH) and downloading software with the Advanced Package Tool or via cloning a github repository.  
You should be comfortable being able to make, delete, navigate and view directories / files with the terminal. However if you don't the commands for such are `$ mkdir <DIRECTORY NAME>`, `$ rm <FILENAME>` / `$ rm -r <DIRECTORY NAME>`, `$ cd <DIRECTORY / FILE NAME>` and `$ ls` respectively (If you have never used commands, or are very unfamilar in how to use these - see the note below about using commands).
Additionally you should be comfortable in installing, updating and upgrading software packages via the Advanced Package Tool (APT). I.e. you should be able to comfortably use the commands  `$ sudo apt-get install <PACKAGE NAME>`, `$ sudo apt update` and `$ sudo apt upgrade`.  
However, if you haven't used these commands all you need to know is the apt make installing software (and all it's subsequent dependencies) much simpler than installing software via source code directly. This is very important with a ROS ecosystem as ROS is designed to be very modular, and when using ROS you can end up with hundreds of packages and as a result even more dependencies! If you were to install it all from source it likely would mean your software wouldn't work at all, wouldn't work well and at the very least will make your project a mess when you want to modifiy / upgrade your systems.  
This is why we use the apt. It makes managing our packages much simpler and easier!  
So when you want to install a package, either for your Linux machine in general, or if it's a ROS package specifically you should check that it can be installed via apt. There are three ways to check.  
1. It will usually say so on the [ROS Wiki](http://wiki.ros.org/) or github repo for the package  
2. You can check in the terminal, try typing out most of the package name and hit the tab key this will complete the package name - or display a list of packages that begin with what you have typed (if they exist on the apt database).  
   For example, if I wanted to see I could install the [joy](http://wiki.ros.org/joy) package I would type `$ sudo apt-get ros-indigo-jo` since joy is a package you can isntall via the apt it will autocomplete it. 
3. Sometimes a package will have a very different name to what you might expect, say you are looking for a specific head file you are missing.  
   The remedy for this is to search the apt database. You can do this by searching on google your package name, and include "ubuntu" with quotations.  
     
When installing a package for ROS we run dependencies we run the command: `$ sudo apt-get install ros-<ROS DISTRO NAME>-<ROS PACKAGE NAME>`

### 1.1.2 Note On Using Commands In This Manual
Any commands that you are to use in the terminal will be in bash and will look like this:  
`$ mkdir hello`    
If the command you are issuing has arguemnts that will be specific to your setup environment, they will look like this:  
`$ mkdir <DIRECTORY NAME>`
You do not need to include the '$' in the command, in fact teh command will not work if you do. The dollar sign is simply included to signify it is a bash command to be issued to your terminal.  
    

### 1.1.2 Robot Operating System  
MARVIN's software systems are based around Robot Operating System (ROS).
This manual will assume that you are familiar with the basic operation and structure of ROS software. For example you should already know that everything within ROS has a node, nodes are typically abstracted from the hardware as much as possible, nodes are designed for one specific purpose and communicate via 'subscribing' and 'publishing' to channels reffered to as topics.  

## 2. MARVIN's Hardware Systems

## 3. MARVIN's Software Systems
