# Project Context

## Purpose

`ros2-robot-motion-lab` is a general ROS 2 robot motion lab for documenting and experimenting with modular robot motion, trajectory planning, and execution.

The repository is intended for study notes, reproducible experiments, validated commands, technical reports, prototype scripts, and future custom ROS 2 packages.

## Current Validation Platform

Doosan Robotics ROS 2 and the Doosan `m1013` are the current experimental validation platform.

Doosan-specific experiments remain valid because they establish a concrete baseline for service-based motion, robot state inspection, MoveIt2 planning, Gazebo simulation, and Python `rclpy` clients.

## Boundary

This repository is intentionally separate from the validated official Doosan workspace:

```text
~/doosan_ws
```

Do not modify, move, copy, or assume control over that workspace from this repository.

## Current Phase

The initial experiment sequence has been completed and documented. The next phase is to define the first minimal ROS 2 package structure without tightly coupling the general layer to Doosan-specific logic.

## Future Package Direction

Future software should distinguish between:

```text
robot_motion_client
doosan_motion_adapter
```

Conceptual responsibilities:

- `robot_motion_client`: general motion request handling, validation flow, and execution orchestration.
- `doosan_motion_adapter`: Doosan-specific communication through official Doosan ROS 2 services and interfaces.

The general layer should avoid direct dependency on Doosan-specific message or service types where possible. Doosan-specific details such as `dsr_msgs2`, `dsr_controller2`, and service paths should remain in the adapter layer.

No ROS 2 package code has been created in this repository yet.

## Validated Doosan Interface

The currently validated Doosan movement service is:

```text
/dsr01/dsr_controller2/motion/move_joint
```

Service type:

```text
dsr_msgs2/srv/MoveJoint
```

This interface should be treated as the first concrete adapter target, not as the full project architecture.

## Documentation Policy

When adding technical notes, prefer documenting:

1. What is being tested or built.
2. Why it matters.
3. What interface, package, or command is involved.
4. What result is expected.
5. What result was obtained.
6. What the next step is.
