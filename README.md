# Robot-Car-Position-Tracking
#  Position Tracking Robot Car using AprilTags

## Overview
This project implements a **real-time position tracking and control system** for a robot car using **AprilTags**.
The system detects the robot’s position and orientation through a camera feed, computes the control signals required to maintain or adjust its position, and sends commands to the robot over a **serial connection** between the python code and the microcontroller of the robot, So centralized control via the laptop.

 Key principles of the project, includes:
- Feedback control (PID)
- localization using AprilTags and camera
- Communication between a PC and a microcontroller
-  Mecanum wheel kinematics for movement control

---

## Software Architecture on Python
The system consists of three main threads: (so it works in parallel)
1. **Serial Thread:** Sends control data packets to the robot.  
2. **Computation Thread:** Runs PID control and updates velocity commands.  
3. **Main Thread:** Handles camera input and AprilTag detection.

---
overall System: 
1. the python code for centralized control
2. the transmitter code from ardunio master nrf
3. the reciver code from arduino slave nrf
---

## Hardware 
- **Robot Car:** Equipped with Mecanum wheels, DC motors and motor driver (L293D)
- **Microcontroller:** Arduino Uno
- **Camera:** USB camera connected to the computer
- **AprilTags:** Printed `tag16h5` family markers
- **Computer:** Running Python for detection and control
- **Communication:** nrf24l01; one connected directly to the PC and the other on the robot.



![Screenshot 2025-11-28 at 9 51 30 PM](https://github.com/user-attachments/assets/a53260ed-f7fb-47de-ab87-598aa4dd9628)

