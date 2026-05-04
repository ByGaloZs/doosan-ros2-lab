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
- Repository phase: initial documentation and structure setup
- ROS 2 package code in this repository: not created yet

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
- Placeholder directories for future packages, scripts, and reports are present.
- `ros2_packages/` is intentionally empty except for its README placeholder.

## Validation Status

The repository currently documents the lab context. Detailed command validation and reproducible experiment results should be recorded separately under:

- `docs/commands/`
- `docs/experiments/`

## Next Step

Document the first validated command or experiment before adding ROS 2 package code.
