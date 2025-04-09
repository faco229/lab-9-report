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

<p align="center">
  <img src="https://github.com/faco229/lab-9-report/blob/main/code1.jpg" width="500">
  <br>
  <b>Figure 1:</b> Modified code part 1
</p>

<p align="center">
  <img src="https://github.com/faco229/lab-9-report/blob/main/code2.jpg" width="500">
  <br>
  <b>Figure 2:</b> Modified code part 2
</p>

<p align="center">
  <img src="https://github.com/faco229/lab-9-report/blob/main/code3.jpg" width="500">
  <br>
  <b>Figure 3:</b> Modified code part 3
</p>

<p align="center">
  <img src="https://github.com/faco229/lab-9-report/blob/main/code4.jpg" width="500">
  <br>
  <b>Figure 4:</b> Modified code part 4
</p>

<p align="center">
  <img src="https://github.com/faco229/lab-9-report/blob/main/code5.jpg" width="500">
  <br>
  <b>Figure 5:</b> Modified code part 5
</p>

<p align="center">
  <img src="https://github.com/faco229/lab-9-report/blob/main/code6.jpg" width="500">
  <br>
  <b>Figure 6:</b> Modified code part 6
</p>

<p align="center">
  <img src="https://github.com/faco229/lab-9-report/blob/main/code7.jpg" width="500">
  <br>
  <b>Figure 7:</b> Modified code part 7
</p>

<p align="center">
  <img src="https://github.com/faco229/lab-9-report/blob/main/code8.jpg" width="500">
  <br>
  <b>Figure 8:</b> Modified code part 8
</p>

In the next part, the PID controller is integrated into the robot's movement to maintain the desired distance from an object. A function is written to move the robot forward or backward based on the measured distance, with the PID library returning an output value that determines the speed and direction of the movement. The system is tuned by adjusting the Kp, Ki, and Kd parameters and tested with the instructor.

See Figure 1 for modiefied code containing Kp, Ki, and Kd values. 

The final part involves implementing a wall-following application, where the PID controller and the orientation of the ultrasonic sensor are modified to maintain a constant distance from a wall while the robot moves. The program is adjusted to allow the left and right wheels to move at different speeds based on the PID output. The PID controller is tuned while the car is on the bench, and a distance sensor is attached to the side of the robot to ensure it maintains the desired distance from the wall while moving at maximum speed. 

Present results to instructor for approval.

---

## Results
Once the code has been modified correctly, the car will correctly sense an object and the wheels will spin away from the object to maintain the pecified distance. Below is a photo of the car being tested.

<p align="center">
  <img src="https://github.com/faco229/lab-9-report/blob/main/car2.jpg" width="300">
  <br>
  <b>Figure 9:</b> Car being stopped by hand
</p>

The car operated correctly, and should was demonstarted to and approved by the instructor.

---

## Discussion

The implementation of the PID controller on the Arduino successfully enabled the robot to maintain a set distance from a wall or object, demonstrating the utility of feedback control systems in real-world robotics. From our tuning process, we observed how each component of the PID—proportional (Kp), integral (Ki), and derivative (Kd)—influences system behavior. Increasing Kp made the robot respond more aggressively to distance errors, which improved reaction time but also introduced more oscillation. Adjusting Ki helped reduce steady-state error but required careful moderation to avoid instability. Finally, tweaking Kd helped smooth the motion and dampen overshoot, improving overall performance during movement and turns.

One major insight gained was the importance of iterative tuning when dealing with physical systems. While theoretical values provided a starting point, real-world testing on the bench and in motion revealed the effects of motor inconsistencies and sensor noise. The use of the map() function to translate PID output into motion direction and speed proved to be an effective strategy to bridge software control and physical response. In the wall-following task, adjusting each motor’s speed based on PID output enabled dynamic and responsive navigation. This highlighted how even simple robots benefit from differential control when navigating complex environments.

---

## Conclusion

This lab reinforced key principles in feedback control systems and offered valuable hands-on experience with PID tuning. By implementing a PID controller on the Arduino platform, we successfully maintained a desired distance from obstacles and walls through real-time sensor feedback and actuator adjustment. The lab demonstrated the importance of proportional, integral, and derivative components in achieving responsive, accurate, and stable behavior in autonomous systems.

The most significant takeaway from this experiment is the practical understanding of how theoretical control algorithms are applied and fine-tuned in real-world systems. This lab also emphasized the value of sensor integration, system modeling, and iterative testing—skills that are foundational in modern control engineering and robotics development.

---

**Citations**

ChatGPT. (2025). Discussion and Conclusion for PID Feedback Controller Lab Report. OpenAI. Retrieved April 9, 2025, from https://chat.openai.com/

Copilot. (2025). Summary of PID Controller Implementation in Robotics Lab. Generated on April 9, 2025, from Quinn’s conversation with copilot. 

Copilot. (2025). Summary of Instruments and Components for PID Control System Implementation. Generated on April 9, 2025, from Quinn’s conversation with copilot. 

---

*End of Lab Report*
