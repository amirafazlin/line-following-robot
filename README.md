# Line-Following Robot with PID Control using Kp, Kd, Ki

## Overview
This project is a line-following robot built using an Arduino Nano, IR sensors, and a motor driver module, with enhanced performance through PID (Proportional-Integral-Derivative) control. The robot follows a dark or light line on a contrasting surface by reading signals from the IR sensors and adjusting motor speeds for precise movement.

## Components Used
- **Arduino UNO** (You can replace it with Arduino NANO if needed)
- **2 DC Motors with Wheels**
- **L298N Motor Driver Module**
- **2 IR Sensor Modules**
- **7 - 12V Lithium Battery**
- **Single Pole Single Throw (SPST) Switch**
- **Jumper Wires**
- **Breadboard**

## Circuit Diagram
The circuit connects the components as follows:

- **IR Sensors**: Connected to Arduino's digital pins for reading line detection
- **L298N Motor Driver**:
  - Input Pins: Connected to Arduino's digital output pins
  - Output Pins: Connected to DC Motors
  - Power Supply: Powered by 7 - 12V batteries
- **DC Motors**: Connected to L298N's output

## How It Works
- The IR sensors detect the line and send signals to the Arduino.
- The Arduino implements a PID control algorithm to minimize line deviation.
- Based on the PID output, the Arduino sends commands to the L298N motor driver.
- The motor driver controls the speed and direction of the DC motors, ensuring smooth and accurate line-following behavior.

## PID Control Explanation
PID control helps the robot adjust its speed and direction more efficiently by considering:
- **Proportional (P)**: How far the robot is from the line.
- **Integral (I)**: Accumulated past errors to correct steady-state errors.
- **Derivative (D)**: Predicts future error to minimize overshooting.

Tuning the PID parameters (Kp, Ki, Kd) allows the robot to follow the line with greater stability and accuracy.

## Code Overview
- Reads input from the IR sensors.
- Computes the error from the line position.
- Applies the PID algorithm to determine motor speed adjustments.
- Controls motor speed and direction through the L298N driver.

## Setup and Installation
1. Assemble the circuit as shown in the diagram.

![LineFollwerRobot](https://github.com/user-attachments/assets/2c17195d-4052-4a5a-937a-0abc6c311854)

2. Upload the Arduino code with PID control to the Arduino Nano using the Arduino IDE.
3. Place the robot on a track with a distinct line.
4. Power on the robot and watch it follow the line smoothly and accurately!

## Troubleshooting
- Ensure IR sensors are properly calibrated.
- Check motor connections and power supply.
- Confirm correct wiring between Arduino, sensors, and motor driver.
