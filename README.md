# Robotics_EV3

Python scripts for Lego Mindstorms EV3 robot control, originally developed for the **Introduction to Vision and Robotics (IVR)** course project at the **University of Edinburgh**. 

This repository provides a collection of modular Python scripts designed to handle essential robotic operations including sensor management, open/closed-loop motion control, dead reckoning (odometry), line following, and obstacle avoidance.

## 🚀 Repository Overview

The codebase is structured with core utility modules, sensor controllers, and primary execution scripts for specific robotic challenges.

### Core Modules & Sensor Control
* **`utilities.py`**: Helper functions and basic mathematical computations used across various control loops.
* **`UltraSensor.py`**: Base interface for managing the Lego EV3 Ultrasonic Sensor.
* **`UScontrol.py`**: Implements high-level logic and control loops based on ultrasonic distance feedback.
* **`odometry.py`**: Tracks the robot's position and orientation (x, y, θ) over time using wheel encoder feedback.
* **`openLoopControl.py`**: Implements raw time-based or step-based movements without sensory feedback loops.

### Autonomous Navigation & Execution Scripts
* **`FollowLine.py`**: Core script handling line-following behaviors using light/color sensors.
* **`Main_obstacle_loop.py`**: Handles obstacle detection and navigation loops using distance thresholds.
* **`Main_curved.py` / `Main_curved2.py`**: Navigation routines optimized for tracking curved lines or paths.
* **`Main_straightLR-A0.py` / `Main_straightLR-A4.py` / `Main_straightLR-A0-4Lines.py`**: Specific variations for navigating straight tracks with varying initial conditions, thresholds, or multiple line configurations.
* **`Main_straightRL.py`**: Dedicated script for straight line navigation configured for Right-to-Left priority.
* **`Main_test.py`**: A playground script used for sanity checks and validating sensor-motor interfaces.

## 📋 Prerequisites & Setup

### Requirements
* **EV3 Hardware**: Lego Mindstorms EV3 Intelligent Brick, motors, ultrasonic sensor, and color/light sensors.
* **Operating System**: [ev3dev](https://ev3dev.org) - A Debian Linux-based operating system designed for the EV3 brick.
* **Language**: Python 3.x with the standard `python-ev3dev` binding library.

### Installation
1. Ensure your EV3 brick is running an updated version of `ev3dev` and is connected via Wi-Fi, Bluetooth, or USB tethering.
2. Clone this repository directly onto your local machine or secure-shell (SSH) into the EV3 brick and clone it there:
```bash
git clone https://github.com
cd Robotics_EV3
```

## 💻 Usage Example

To run a specific navigation profile (for example, executing the primary line-following logic), execute the target script directly via your terminal or inside an established SSH session on the brick:

```bash
python3 FollowLine.py
```

*Note: Make sure that scripts interacting directly with hardware peripherals have execution permissions granted (`chmod +x <script_name>.py`) and include the appropriate shebang line (`#!/usr/bin/env python3`) at the top of the file.*

## 🛠️ Built With

* [Python](https://python.org) - Primary programming language.
* [ev3dev API](https://readthedocs.io) - Linux kernel drivers and Python libraries interface for Lego Mindstorms.
