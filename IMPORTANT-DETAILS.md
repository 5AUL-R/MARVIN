# Network and router settings  
- Marvin's wireless network SSID: MARVIN
- Marvin's wireless network password: "        " (8 spaces)  
Details for modifying network:  
Network configuartion ip: http://tplinklogin.net  
Login: admin  
Password: admin  
**when making changes that require a reboot of the router - the NUC must also be rebooted before the configuration page can be accessed**  
# Troubleshooting notes  
## $ roscore doesn't run  
It's critical for ROS to have a correctly configured network.  
The cornerstone of correctly configuring the network for ROS is ensuring that the ip address of the host is specified, as this is required for ROS's core service (roscore)  
**Modifying network settings can interefere with this**  
if $ roscore fails you will be met with an error along the lines of:  
  
"unable to connect to my own server at [http://marvin:52553/].  
This usually means that the network is not configured properly.  
A common cause is that the machine cannot ping itself, Please check for errors by running $ ping marvin  
For more tips, please see:  
(http://www.ros.org/wiki/ROS/NetworkSetup)[http://www.ros.org/wiki/ROS/NetworkSetup]  
the traceback error was written to the log file"  
  
To fix this error you will need to take the following steps:  
1. Try to ping the host (marvin) as the error instructs  
2. If the ping results in 100% packet loss (it doesn't work) you will need to run the following command:  
$ ifconfig  
This will give you a list of network information for your device. The important details will be under the section: wlan0  
This section is the network interface info for the device's wireless card.  

3. In wlan0, find the ip address listed next to "inet addr:" 
Copy that IP address, as this is the ip address of the machine.  
4. Ping that ip address, so run: $ ping <IP_ADDR>  
IN our case, <IP_ADDR> is the IP address from above that you will have copied.  
5. You should be greeted with a message stating how long <IP_ADDR> took to ping. This means our found IP is defintely the one we are looking for, now we need to tell ROS this is the IP of our host that it needs:
6. Run $ echo export ROS_MASTER_URI=http://<IP_ADDR>:11311 >> ~/.bashrc  
7. Run $ echo export ROS_HOSTNAME=<IP_ADDR>:11311 >> ~/.bashrc  
8. Now you should have sucessfully changed the host IP that ROS is using to the actual IP of your host machine. Ensure it's worked by running $ roscore  


