# Autonomous ESP32 Rover

> An ESP32-powered autonomous mobile robot combining real-time video streaming, LiDAR-based obstacle detection, and multiple driving modes through a browser-based control dashboard.

---

## Overview

The Autonomous ESP32 Rover is an embedded robotics platform designed for both manual and autonomous navigation.

The system combines an **ESP32-CAM** for live video streaming with an **ESP32 controller** responsible for motor control, LiDAR processing, and autonomous obstacle avoidance.

A browser-based dashboard provides multiple driving methods, allowing the rover to be controlled remotely over WiFi without requiring any dedicated application.

---

# Features

### Live Video Streaming

- ESP32-CAM real-time video streaming
- Browser-based monitoring
- Low-latency WiFi transmission

---

### Multiple Control Modes

The rover supports several driving methods from a single web dashboard.

#### Manual Control

- Forward
- Backward
- Left
- Right
- Stop

---

#### Phone Gyroscope Steering

Drive the rover by tilting the mobile phone.

- Motion-based steering
- Hands-free directional control
- Real-time orientation updates

---

#### Autonomous Mode

The rover can navigate independently using onboard sensors.

- TFmini LiDAR obstacle detection
- Distance-based navigation
- Automatic obstacle avoidance
- Continuous environment scanning

---

## Hardware

### Controller

- ESP32

### Camera

- ESP32-CAM

### Distance Sensor

- TFmini LiDAR

### Motor Driver

- L298N Motor Driver

### Chassis

- Differential drive mobile platform

---

# System Architecture

```
                  Web Dashboard
                        │
        ┌───────────────┴───────────────┐
        │                               │
   ESP32-CAM                    ESP32 Controller
 Live Video Stream              Motor Controller
        │                               │
        │                         TFmini LiDAR
        │                               │
        └──────────────┬────────────────┘
                       │
                  L298N Driver
                       │
                    DC Motors
```

---

# Control Dashboard

The web dashboard provides:

- Live camera feed
- Manual driving buttons
- Mobile gyroscope steering
- Autonomous mode toggle
- Emergency stop

Everything runs directly inside a web browser over WiFi.

---

# Autonomous Navigation

The autonomous mode continuously reads distance data from the TFmini LiDAR sensor.

The rover:

- scans the environment
- detects nearby obstacles
- determines a safe direction
- adjusts movement automatically

No external computer is required.

---

# Technologies

### Hardware

- ESP32
- ESP32-CAM
- TFmini LiDAR
- L298N Motor Driver
- DC Motors

### Software

- Arduino C++
- WiFi Networking
- Embedded Web Server
- Sensor Integration
- Real-Time Motor Control

---

# Applications

- Autonomous Robotics
- Remote Surveillance
- Indoor Navigation
- Robotics Education
- Embedded Systems Learning

---

# Future Improvements

- SLAM-based mapping
- Object detection using Edge AI
- Autonomous waypoint navigation
- ROS integration
- Voice control
- Cloud telemetry
- GPS-based outdoor navigation

---

# Learning Outcomes

This project provided practical experience in:

- Embedded firmware development
- Robotics
- LiDAR sensor integration
- WiFi networking
- Browser-based control systems
- Real-time motor control
- Autonomous navigation algorithms
- Embedded web application development

---

## Author

**Vamshi Krishna**

GitHub: https://github.com/Jvkrog
