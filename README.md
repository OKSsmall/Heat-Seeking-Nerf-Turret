# AutoAim Nerf Turret

A Raspberry Pi-powered nerf turret that detects moving people and automatically aims and fires a minigun-style blaster.

This project is designed as a portfolio build that combines computer vision, robotics, networking, and embedded system control.

## Project Summary

The system uses a PC or Raspberry Pi camera to detect a moving target, calculates aiming angles, and sends commands to a Raspberry Pi that controls the pan/tilt servos and firing trigger.

Key features:
- Real-time detection and tracking
- Distributed architecture: vision on PC, hardware control on Raspberry Pi
- Pan/tilt servo aiming system
- Minigun-style nerf blaster trigger actuation
- Modular software structure with room for future upgrades

## Why this project?

This project is designed to kick off my GitHub Portfolio, it showcaes: 
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

## Materials List

The full materials list is maintained separately in `MATERIALS.md`, but the major components are:
- Raspberry Pi 4 (recommended 4GB+)
- Raspberry Pi Camera Module 3
- 2x pan/tilt servos (MG996R or equivalent)
- 1x fire trigger servo
- XSHOT minigun-style nerf blaster
- Power supply for Raspberry Pi and servos
- Mounting hardware and 3D printed brackets
- System cables, jumper wires, and connectors

## Project Phases

### Phase 1 — Setup and prototyping
- Set up Raspberry Pi OS and camera support
- Run a basic camera capture test
- Install Python, OpenCV, and supporting libraries
- Create a simple target detection script

### Phase 2 — Tracking and control
- Implement target tracking logic
- Build a pan/tilt test rig
- Confirm servo movement and calibration
- Add networking between PC and Raspberry Pi
- Validate command transmission and response

### Phase 3 — Integration and testing
- Mount the XSHOT blaster onto the rig
- Tune aiming and trigger timing
- Test with moving targets in a controlled environment
- Add safety limits and timeout logic

## Usage

The initial workflow will look like this:

1. Start the Raspberry Pi control server.
2. Run the vision and tracking code on the PC or Raspberry Pi.
3. Watch the turret aim at detected targets.
4. Fire the trigger once the target is aligned.

## Safety Notes

This project is a demonstration and should only be used in a safe environment:
- Use foam darts only
- Always wear eye protection
- Do not aim at people’s faces or animals
- Keep the workspace clear of bystanders

## Next steps

- Create the detailed software layout
- Build the control and networking modules
- Start with the basic camera and detection script
- Add documentation for setup and calibration

---

**Project status:** In development

**Owner:** OKSsmall
