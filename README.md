# Heat-Seeking Nerf Turret

A Raspberry Pi-powered nerf turret that detects moving people and automatically aims and fires a minigun-style blaster.

This project is designed as a portfolio build that combines computer vision, robotics, networking, and embedded system control.

## Project Summary

The system uses a PC or Raspberry Pi camera to detect a moving target, calculates aiming angles, and sends commands to a Raspberry Pi that controls the pan/tilt servos and firing trigger.

Key features:
- Real-time person detection and tracking
- Distributed architecture: vision on PC, hardware control on Raspberry Pi
- Pan/tilt servo aiming system
- Minigun-style nerf blaster trigger actuation
- Modular software structure with room for future upgrades

## Why this project?

This build demonstrates several portfolio-worthy skills:
- Computer vision with Python and OpenCV
- Real-time object tracking and pose estimation
- Raspberry Pi GPIO control for servos
- Networked communication between devices
- Mechanical design and electronics integration
- Documentation, testing, and system calibration

## Architecture Overview

The system is split into two main parts:

1. **Vision and tracking**
   - Detect targets from camera feed
   - Track the selected target across frames
   - Convert image coordinates to pan/tilt angles
   - Send commands to the Raspberry Pi over the local network

2. **Hardware control**
   - Receive pan/tilt/fire commands
   - Drive servo motors to aim the turret
   - Activate a fire servo to pull the trigger


## Safety Notes

This project is a demonstration and should only be used in a safe environment:
- Use foam darts only
- Always wear eye protection
- Do not aim at people’s faces or animals
- Keep the workspace clear of bystanders

## Current Status:
Currently detects motion on webcam feed, NOT the raspberry PI
Motion detection is incredibly consistent
Works flawlessly in well-lit areas, but suffers in dim lighting
Git repo initialized


---

**Project status:** In development

**Owner:** OKSsmall
