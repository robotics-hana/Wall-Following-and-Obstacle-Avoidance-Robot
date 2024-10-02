# Wall-Following and Obstacle Avoidance Robot

This project involves an Arduino-based robot capable of following walls and avoiding obstacles using a combination of ultrasonic sensors, a servo motor, and L298N motor drivers. The robot detects its surroundings and maneuvers accordingly, ensuring smooth navigation without collisions.

## Table of Contents
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Wiring](#wiring)
- [Code Overview](#code-overview)
- [Installation](#installation)
- [Usage](#usage)

## Hardware Requirements
- Arduino Uno (or compatible)
- 2 DC motors with wheels
- L298N Dual H-Bridge Motor Controller
- Ultrasonic Sensor (HC-SR04)
- Servo motor
- Buzzer
- 9V battery or power supply
- Jumper wires
- Breadboard

## Software Requirements
- Arduino IDE (latest version)
- Servo library (pre-installed with Arduino IDE)

## Wiring

- **Motors**:
  - Right motor direction pins: D12 (IN1), D11 (IN2)
  - Left motor direction pins: D7 (IN3), D8 (IN4)
  - Right motor speed pin: D3 (ENA)
  - Left motor speed pin: D6 (ENB)
  
- **Ultrasonic Sensor**:
  - Trig pin: D10
  - Echo pin: D2
  
- **Servo**:
  - Servo pin: D9
  
- **Buzzer**:
  - Buzzer pin: D13

## Code Overview

### Movement Functions:
- **`go_Advance()`**: Moves the robot forward.
- **`go_Left()`**: Turns the robot left.
- **`go_Right()`**: Turns the robot right.
- **`go_Back()`**: Moves the robot backward.
- **`stop_Stop()`**: Stops the robot.

### Sensor Functions:
- **`watch()`**: Measures distance using the ultrasonic sensor.
- **`watchsurrounding()`**: Scans the surroundings and assigns distance values to variables for left, right, front, and diagonal directions.
  
### Motor Speed Control:
- **`set_Motorspeed(speed_L, speed_R)`**: Sets the motor speed for left and right motors.

### Obstacle Avoidance:
- The robot continuously monitors its surroundings using the ultrasonic sensor and servo. Based on the obstacle distance, it adjusts its movement to avoid collisions and follow walls.

## Installation
1. Download and install the Arduino IDE.
2. Connect the robot components as per the wiring diagram.
3. Upload the provided code to your Arduino board using the Arduino IDE.

## Usage
1. Power the robot using a 9V battery or an external power source.
2. Place the robot in a space where it can move freely.
3. The robot will start following walls and avoiding obstacles based on the distances measured by the ultrasonic sensor.

### Example Commands:
- **Wall following**: The robot will maintain a set distance from the wall as it moves.
- **Obstacle Avoidance**: Upon detecting an obstacle, the robot will adjust its path to avoid a collision.

Project uses parts of Osyoo Code, please see the website for more information HTTPS ://osoyoo.com/
