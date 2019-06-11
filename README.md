# 2019_STMouse

## Overview 👁️
The assumption of the project is to create a glove that acts as a computer mouse. This allow to easily use computer, using hand gestures, at a distance from the work station (limited by the length  of the cables).
## Description 📋
### Software
STMouse 1.0.2 Anakonda, an application on STM32.
## Hardware
1. 10DOF module with an intelligent BOR055 orientation sensor BNO055 (accelerometer, guroscope and magnetometer) and a BMP280 pressure sensor equipped with a Gravity connector, sewn onto the glove. The module is connected using the I2C interface, consisting of four wires.
2. Four buttons (on each finger except the small one). Each button is connected with two wires - supply and return with information about it's condition.
3. An UTP cable with length of 3 meters with an additional nineth wire, connecting the microcontroller with the glove.
4. STM32F407G-DISC1 [STMicroelectronics](https://www.st.com/en/microcontrollers-microprocessors/stm32f407-417.html).
## Tools 🛠️
### Software
1. STM32CubeMX v4.27.0
2. System Workbench for STM32 (Neon.3 Release v4.6.3)
3. STMStudio v3.6.0 (for debugging)
4. ST-LinkUpgrade  

## How to run ⚙️
1. Everything you need is an HID driver installed on your computer, every opereting system should have it.
2. Thumb button - lock/unlock STMouse.
   Index finger button - left mouse button
   Middle finger button - middle mouse button
   Ring finger - right mouse button
3. Diodes on the microcontroller:
   Green - at the start of the program if a gyroscope is connected.
   Orange - when the mouse works and send a signal to the computer.
   Red - when the axes are reversed.
   Blue - changes it's state when you press any button.
### Connections to STM32F407G
Two USB cables, one for power supply and the other for the HID communication.
## How to compile 💻
Import project to System Workbench and click on 'RUN' button. Everything should be upload to STM32. Microcontroller should be connected to the computer. 
## Bugs 
The BNO055 system occasionally makes erroneous measurements of overloads, recording the maximum values of these parameters.
## Future improvements ✏️
There are many potentil project development opportunities, among others: 
- Wireless communication, increasing the convenience of movement. 
- Improving the resposiveness of the device.
- More buttons and gestures ensuring additional functionalities such as opening     selected programs, sound control. 
- An interesting prospect of development could be adding a second glove that adds   additional functions depending on the distance and movements of both hands, for   example, moving away from each other it could dismiss the view and bringing them   closer - zooming the view.
## Addition 💡
  The project used a library for the module BNo055 created by the github user bugratufan and published here: https://github.com/bugratufan/STM32_BNO055/?fbclid=IwAR2R_Ds-xPxk-i865TxB8s8_3m9aMgMNJ85il7Vmm2JdS2bNgLOdiO4vQnI.
  The project was conducted during the Microprocessor Lab course held by the Institute of Control and Information Engineering, Poznan University of Technology. Supervisor: Adam Bondyra.

