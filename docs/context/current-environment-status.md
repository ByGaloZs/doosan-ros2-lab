# Current Environment Status

## Purpose

Track the known local environment status for this lab repository.

## Scope

This document describes the environment used for `doosan-ros2-lab` only.

Do not treat this repository as the validated official Doosan workspace. The official validated workspace remains separate at:

```text
~/doosan_ws
```

## Current Status

- Operating system: Ubuntu 24.04 LTS
- ROS 2 distribution: Jazzy
- Doosan Robotics ROS 2: installed in the separate validated workspace
- Robot model used for experiments: Doosan `m1013`
- Repository phase: completed initial experiment sequence
- ROS 2 package code in this repository: not created yet
- Prototype scripts in this repository: one Python `rclpy` service client prototype

## Known Tools Mentioned For This Lab

- ROS 2 Jazzy
- Doosan Robotics ROS 2
- RViz2
- MoveIt2
- Gazebo
- Docker-based Doosan emulator
- Python / `rclpy`

## Repository Status

- Documentation directories are present.
- Experiment documentation is present under `docs/experiments/`.
- A prototype script is present under `scripts/prototypes/`.
- `ros2_packages/` is intentionally empty except for its README placeholder.

## Validation Status

The initial experiment sequence has been completed and documented under:

- `docs/commands/`
- `docs/experiments/`

Validated areas include:

- direct `MoveJoint` service control;
- ROS 2 graph and robot state inspection;
- Doosan service and interface mapping;
- `MoveLine` Cartesian motion;
- MoveIt2 planning and execution;
- Gazebo simulation;
- motion command failure handling;
- a Python `rclpy` service client prototype.

## Next Step

Prepare the first custom ROS 2 package under `ros2_packages/` only after deciding the minimal package structure for `doosan_motion_client`.
