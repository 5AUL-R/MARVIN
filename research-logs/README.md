This is where I'll place more in depth descriptions of things I find  

# Movement control  
To get MARVIN to move under remote control from a 360 controller the following needs to be done:  
1. Turn on the NUC  
2. Turn on the RMP:  
Press and hold the green button for 5 seconds  
Press and hold the yellow button for 5 seconds
Lift MARVIN so that he is perpindicular to the ground  
Press and hold the dynamic stabilisation button  
3. Start the software:  
Run $ roscore
Run (in a new terminal) $ roslaunch marvin_control marvin_full.launch  
Turn on the xbox 360 controller (ensure it is paired with the dongle attahced to MARVIN)

# Eye colour control
# Torso and head control
## Items to do   
1. Check the fuses on the control board, have the blown?  
2. Check the voltage to be supplied to the control board, is the USB connection sufficient, or does it require the jack as well?  
3. Additionally, ensure the usb connection works (the wire has continuity).
