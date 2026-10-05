# ROBOTBRAIN

An ESP32-based robot board that integrates two L293DD ICs to control four DC motor outputs. Also has an integrated magnetometer (LIS3MDL) for direction control. 

## Why? 

Last year for Science Olympiad's Robot Tour event, I designed an omnidirectional robot with tons of features, and importantly, many of them were based on QFN packages and a very weak LDO. 
This time I'm doing better. 5A LDO. No QFN (except the magnetometer). Proper power regulation. 
This will be the better robot. 

## What's changed? 

The previous version also contained a LSM6DSOX IC which has been scrapped since the SciOly robot can't effectively use linear and rotational acceleration data (too much drift). However magnetic field helps with absolute positioning. 
The previous version used a 1A LDO which was too little for three motors. This uses a 5A LDO which is plenty for 4 motors. The motor drivers have been upgraded to large L293DD packages to account for the higher current load. 
The power switching system has been significantly simplified, using a physical switch to alternate between battery power and USB power. There is no integrated battery charging since the robot is designed to use 8xAA (12V) instead of a 3.7V LiPo. 
Has an extra button to calibrate and start the robot because it may be easier than resetting. can be used to toggle on/off instead of robot running every time code uploads. 

## Known Issues
The current revision of the board lacks I2C pull up resistors, and so the sensors don't work. If you plan on making this project, please add those pull ups!

## Images

![sch](https://github.com/Omegon0/robotbrain/blob/main/sch.jpg?raw=true)
![pcb](https://github.com/Omegon0/robotbrain/blob/main/pcb.jpg?raw=true)
![rend1](https://github.com/Omegon0/robotbrain/blob/main/rend1.jpg?raw=true)
![rend2](https://github.com/Omegon0/robotbrain/blob/main/rend2.jpg?raw=true)
