# Autonomous Indoor Surveillance Robot

## 📌 Project Overview

An autonomous indoor surveillance robot designed to continuously patrol indoor environments while providing live video monitoring of the environment.

The robot integrates embedded systems, multiple sensors, motor control, computer vision, and wireless communication to enable autonomous movement, obstacle avoidance, environmental monitoring, and safety alerts.

This project was developed as a graduation project in Intelligent Systems Engineering.

## 🎯 Project Characteristics

The main features of the project are:

* an autonomous indoor surveillance robot capable of doing continuous patrol.
* detects obstacles and avoid them using multiple ultrasonic sensors.
* Provide live video monitoring through a camera.
* Integrate computer vision for detecting objects in front of the robot.
* Implement a fire detection and alert system using a flame sensor and buzzer.
* Monitor the robot's movement using an IMU to detect stuck conditions.
* Integrate Arduino and Raspberry Pi for low-level control and high-level processing.

## 🧠 System Architecture and Components

The autonomous surveillance robot is designed as an integrated system consisting of several functional groups. Each group is responsible for a specific task such as sensing, processing, movement, monitoring or power supply

### Sensing

#### Ultrasonic Sensors
used for obstacle detection and collision avoidance.
    
#### Flame Sensor
  Detects the presence of flame or fire in front of or near the robot.

#### IMU Sensor / Gyroscope
Detects motion changes and acceleration variations to determine whether the robot is moving normally or stuck.

### Processing

#### Arduino Uno (The muscle) 
It reads sensors, controls the motors, handles obstacle avoidance logic

#### Raspberry Pi (the brain)
It handles camera streaming, computer vision processing, and communication with the user interface.
