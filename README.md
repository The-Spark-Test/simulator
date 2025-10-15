# SPARK Simulator

## Overview

The **Simulator** module provides a virtual testing environment for humanoid robots, enabling motion emulation and sensor data generation. It allows SPARK to test robots in simulated physics environments before real-world trials.

## Features

- Physics-based humanoid simulation environment
- Supports ROS or Gazebo-style integration
- Realistic motion, balance, and sensor emulation
- Data export for analysis and evaluation
- Configurable simulation scenarios
- Multi-robot testing capabilities
- Real-time and batch simulation modes

## Architecture

```
simulator/
├── environments/         # Configurable simulation scenarios
├── physics/              # Motion and kinetics engine
├── sensors/              # Vision, lidar, and tactile sensor models
├── exporters/            # Data formatters for evaluation
├── scripts/              # Simulation runners
├── config/               # Configuration files
├── tests/                # Unit and integration tests
└── main.py               # Entry point for simulation
```

## Tech Stack

- **Language:** Python 3.11+
- **Physics Engines:** PyBullet, MuJoCo, Gazebo
- **Libraries:** ROSPy, NumPy, Pandas, OpenCV
- **Visualization:** Matplotlib, Open3D

## Installation

```bash
# Clone the repository
git clone <repository-url>
cd spark_simulator

# Install dependencies
pip install -r requirements.txt

# Install physics engine (choose one)
pip install pybullet  # or
pip install mujoco

# Run tests
python -m pytest tests/
```

## Usage

```python
from simulator import environments, physics, sensors

# Example usage
env = environments.HumanoidEnvironment()
robot = physics.HumanoidRobot(env)
sensor_data = sensors.capture_data(robot)
```

## Simulation Scenarios

1. **Locomotion Tests** - Walking, running, climbing
2. **Manipulation Tasks** - Object handling, tool use
3. **Balance Challenges** - Uneven terrain, disturbances
4. **Coordination Exercises** - Multi-limb tasks
5. **Adaptation Scenarios** - Dynamic environments
6. **Efficiency Tests** - Energy consumption analysis
7. **Reliability Trials** - Stress testing and failure modes

## Integration

- Provides motion and sensor data to `evaluation/`
- Interfaces with `robot-interface/` for hybrid (real + sim) testing
- Accessible through `api/` for simulation-as-a-service

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Submit a pull request

## License

[Add license information here]
