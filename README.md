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

#### • Ultrasonic Sensors
used for obstacle detection and collision avoidance.
    
#### • Flame Sensor
Detects the presence of flame or fire in front of or near the robot.

#### • IMU Sensor / Gyroscope
Detects motion changes and acceleration variations to determine whether the robot is moving normally or stuck.

### Processing

#### • Arduino Uno (The muscle) 
It reads sensors, controls the motors, handles obstacle avoidance logic

#### • Raspberry Pi (the brain)
It handles camera streaming, computer vision processing, and communication with the user interface.

### Actuation

#### • DC Motors
Provide the main movement of the robot, allowing it to move forward, backward, and turn.

#### • Motor Driver
controls motors direction and speed.

#### • Wheels
Transfer motor rotation into robot motion.

#### • Robot Chassis
Provides the mechanical structure that carries and supports all components.

### Monitoring

#### • Camera Module
Captures live video for surveillance and monitoring.

#### • Waveshare Screen
provide a local display for monitoring, testing, and system visualization directly on the robot.

#### • User Interface (UI)
Displays the live camera feed, object detection output, and system alerts to the user.

### Power

#### • Battery Pack
Supplies power to the whole robot system

#### • Voltage Regulator
Converts the battery voltage to suitable levels for components such as the Arduino, Raspberry Pi, sensors.

#### • Toggle Switch
Activates or deactivates the Arduino control code during operation.

#### • Power Distribution Wiring
Distributes electrical power to motors, sensors, and other modules.

### Communication

#### • Arduino–Raspberry Pi Communication
Allows coordination of work between low-level control and high-level processing


## 🚗 Operation

The robot operates using a continuous closed-loop strategy that combines movement, sensing, and monitoring. During normal operation, the robot moves forward while the ultrasonic sensors continuously measure the distance to nearby obstacles. The front ultrasonic sensor uses a safety threshold of 50 cm, allowing the robot to stop early enough before collision and providing sufficient space for turning.
When an obstacle is detected within the threshold distance, the robot stops and evaluates the available space on the right and left sides. It then selects the direction with the greater free space and starts turning. The turning process is controlled using a smart strategy, where the robot continues turning until the side ultrasonic sensor reads approximately the same distance previously measured by the front sensor, with a tolerance of ± 3 cm. This allows more controlled turning compared with using a fixed turning time only. While the robot is moving, the camera continuously captures live video and streams it to the user interface

## 🔥 Flame Detection System

a flame sensor and buzzer were added to introduce a safety and emergency response feature. The system was programmed so that when the robot detects a flame, it immediately stops, activates the alarm, and sends an alert to the user interface. The robot does not continue moving until the user gives permission through the interface. This feature improves operational safety

## 🧭 IMU Based Movement

An IMU / gyroscope is used to monitor the robot's movement and detect situations where the robot may become stuck.
When an abnormal movement condition is detected, the robot perform a turning around to improve operational effiency

## 🖥️ User Interface

A user interface was developed to provide the user with the remote monitoring capabilities

The interface allows the user to:

• Monitor the live camera stream.

• Receive system alerts.

• Monitor important robot conditions

## 📷 Project Photos

![Robot Prototype](images/Model_Photo.jpg)
