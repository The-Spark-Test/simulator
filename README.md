# SPARK Simulator

## Overview

The **Simulator** module provides a virtual testing environment for humanoid robots, enabling motion emulation and sensor data generation.  
It allows SPARK to test robots in simulated physics environments before real-world trials.

## Features

- Physics-based humanoid simulation environment
- Supports ROS or Gazebo-style integration
- Realistic motion, balance, and sensor emulation
- Data export for analysis and evaluation

## Architecture

simulator/
├── environments/ # Configurable simulation scenarios
├── physics/ # Motion and kinetics engine
├── sensors/ # Vision, lidar, and tactile sensor models
├── exporters/ # Data formatters for evaluation
├── scripts/ # Simulation runners
└── main.py

## Tech Stack

- **Python 3.11+**
- **Libraries:** PyBullet / MuJoCo / ROSPy, NumPy, Pandas

## Integration

- Provides motion and sensor data to `evaluation/`
- Interfaces with `robot-interface/` for hybrid (real + sim) testing
- Accessible through `api/` for simulation-as-a-service
