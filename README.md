# Line-Following Robot with PID Control using Kp, Kd, Ki

## Overview
This project is a line-following robot built using an Arduino Nano, IR sensors, and a motor driver module, with enhanced performance through PID (Proportional-Integral-Derivative) control. The robot follows a dark or light line on a contrasting surface by reading signals from the IR sensors and adjusting motor speeds for precise movement.

## Components Used
- **Arduino Nano** (You can replace it with Arduino Uno if needed)
- **2 DC Motors with Wheels**
- **L298N Motor Driver Module**
- **3 IR Sensor Modules**
- **2 x 11.1V Lithium Battery**
- **Single Pole Single Throw (SPST) Switch**
- **Breadboard and Jumper Wires**

## Circuit Diagram
The circuit connects the components as follows:

- **IR Sensors**: Connected to Arduino's digital pins for reading line detection
- **L298N Motor Driver**:
  - Input Pins: Connected to Arduino's digital output pins
  - Output Pins: Connected to DC Motors
  - Power Supply: Powered by 9V batteries
- **DC Motors**: Connected to L298N's output
- **Power Supply**: Two 11.1V batteries wired to both the motor driver and the Arduino

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

![circuit_image](https://github.com/user-attachments/assets/4c5dcb79-98a3-4f0e-a9c0-03a800c1d9a9)

2. Upload the Arduino code with PID control to the Arduino Nano using the Arduino IDE.
3. Place the robot on a track with a distinct line.
4. Power on the robot and watch it follow the line smoothly and accurately!

## Troubleshooting
- Ensure IR sensors are properly calibrated.
- Tune the PID parameters (Kp, Ki, Kd) for optimal performance.
- Check motor connections and power supply.
- Confirm correct wiring between Arduino, sensors, and motor driver.

