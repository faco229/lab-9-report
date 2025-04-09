# lab-9-report

**Names of People Involved (Group Members):**  
Faith Cox & Quinn Rison 

**Date Submitted:**  
4/9/2025

---

## Introduction / Summary

This lab involves implementing a control system to maintain a robot at a specified distance from an object using an ultrasonic distance module as the sensor and car motors as the actuators. A proportional-integral-derivative (PID) controller will be implemented and tuned on an Arduino to achieve this goal. The PID controller, a process developed in the 1600s to control the speed of a grain feeder, is now widely used in various industries. It calculates the error between the desired value (setpoint) and the measured value, feeding this error into an amplifier, an integrator, and a differentiator. The outputs are summed and applied to the process actuator, with each block containing a parameter that adjusts its effect on the overall process. Many microcontrollers, including Arduino devices, can run the PID library, which will be utilized in this lab.

---

## Methods / Tests
For this laboratory exercise, several instruments and components are required, including a computer running Arduino IDE and Chrome Browser, and the SparkFun Inventor’s Kit, which contains a RedBoard, an ultrasonic sensor, two motors, a motor driver, and a battery pack. The exercise involves implementing a PID control system using the distance measurement from the ultrasonic sensor. The process begins with installing the PID_v2 Library in the Arduino IDE and modifying the robot sketch to include the library, define necessary variables, create a PID instance, and initialize the PID within the setup function. The PID is then run within the loop function to compute the output based on the tuning and inputs, and the setpoint, measurement, and output values are written to the serial port for verification.

Photo of Code with variables and loop function

In the next part, the PID controller is integrated into the robot's movement to maintain the desired distance from an object. A function is written to move the robot forward or backward based on the measured distance, with the PID library returning an output value that determines the speed and direction of the movement. The system is tuned by adjusting the Kp, Ki, and Kd parameters and tested with the instructor.

Photo of robot in testing and kp ki kd parameters in the code

The final part involves implementing a wall-following application, where the PID controller and the orientation of the ultrasonic sensor are modified to maintain a constant distance from a wall while the robot moves. The program is adjusted to allow the left and right wheels to move at different speeds based on the PID output. The PID controller is tuned while the car is on the bench, and a distance sensor is attached to the side of the robot to ensure it maintains the desired distance from the wall while moving at maximum speed.

Photo of the car and wall in this test

<p align="center">
  <img src="" width="500">
  <br>
  <b>Figure 1:</b> MEASURING TRUE RESISTOR MEASUREMENTS
</p>


---

## Results

---

## Discussion



---

## Conclusion


---

**Citations**



---

*End of Lab Report*
