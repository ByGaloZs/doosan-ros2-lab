# Project Context

## Purpose

`doosan-ros2-lab` is a technical lab for documenting and experimenting with ROS 2 Jazzy and Doosan Robotics ROS 2 using the Doosan `m1013` as the experimental platform.

The repository is intended for study notes, reproducible experiments, validated commands, technical reports, and future custom ROS 2 packages.

## Boundary

This repository is intentionally separate from the validated official Doosan workspace:

```text
~/doosan_ws
```

Do not modify, move, copy, or assume control over that workspace from this repository.

## Current Phase

The project is in the initial documentation and structure phase.

Current priorities:

1. Keep the repository clean.
2. Document the validated environment.
3. Build ROS 2 and Doosan study notes.
4. Record tested commands.
5. Create reproducible experiment notes.
6. Prepare future custom ROS 2 packages incrementally.

## Future Package Direction

A future custom package may be created under `ros2_packages/` with a name such as:

```text
doosan_motion_client
```

That package should favor direct use of official ROS 2 and Doosan interfaces, especially:

- `dsr_msgs2`
- `dsr_controller2`
- official ROS 2 services
- Python / `rclpy`

No ROS 2 package code has been created in this repository yet.

## Validated Doosan Interface

The movement service currently documented for future experiments is:

```text
/dsr01/dsr_controller2/motion/move_joint
```

Service type:

```text
dsr_msgs2/srv/MoveJoint
```

Future experiments should validate usage directly and document the result under `docs/experiments/`.

## Documentation Policy

When adding technical notes, prefer documenting:

1. What is being tested or built.
2. Why it matters.
3. What interface, package, or command is involved.
4. What result is expected.
5. What result was obtained.
6. What the next step is.
