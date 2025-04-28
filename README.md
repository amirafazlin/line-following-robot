# Line-Following Robot 

## Overview
This project is a line-following robot built using an Arduino Nano, IR sensors, and a motor driver module. The robot follows a dark or light line on a contrasting surface by reading signals from the IR sensors and adjusting motor speeds for precise movement.

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
- The IR sensors detect the line (black line on white surface) and send signals (HIGH/LOW) to the Arduino.
- The Arduino reads the sensor signals and makes simple decisions:
  - If both sensors detect black, the robot moves forward.
  - If left sensor detects black and right sensor detects white, the robot turns left.
  - If right sensor detects black and left sensor detects white, the robot turns right.
  - If both sensors detect white, the robot stops.
  - The Arduino sends basic control signals to the L298N motor driver.
- The motor driver drives the DC motors accordingly, allowing the robot to follow the line.

## Code Overview
- Reads input signals from the left and right IR sensors.
- Determines the robot’s movement direction based on the sensor readings.
- Commands the motors to move forward, turn left, turn right, or stop accordingly.
- Controls motor direction and speed through the L298N motor driver.

## Setup and Installation
1. Assemble the circuit as shown in the diagram.

![LineFollwerRobot](https://github.com/user-attachments/assets/2c17195d-4052-4a5a-937a-0abc6c311854)

2. Upload the Arduino code to Arduino UNO using the Arduino IDE.
3. Place the robot on a track with a distinct line.
4. Power on the robot and watch it follow the line smoothly and accurately!

## Troubleshooting
- Ensure IR sensors are properly calibrated.
- Check motor connections and power supply.
- Confirm correct wiring between Arduino, sensors, and motor driver.
