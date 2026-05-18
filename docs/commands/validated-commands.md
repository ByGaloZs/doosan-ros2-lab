# Validated Commands

This document records commands that have been tested and validated in the local ROS 2 / Doosan Robotics environment.

The goal is not to collect every possible command, but to keep a reliable list of commands that are useful, understood, and reproducible.

## Rules

Before adding a command to this file, make sure that:

- the command was tested locally;
- the purpose is clear;
- the expected result is known;
- the command is relevant to this lab;
- the command does not modify the official Doosan workspace unless explicitly intended.

The official validated Doosan workspace is:

```text
~/doosan_ws
```

This repository must remain separate from that workspace.

---

## Repository Commands

### Check repository status

#### Purpose

Check the current Git status of this repository.

#### Command

```bash
git status
```

#### Expected Result

Git should show the current branch and whether there are modified, staged, or untracked files.

#### Notes

Useful before committing documentation changes.

---

## Docker Commands

### Check Docker installation

#### Purpose

Verify that Docker is installed.

#### Command

```bash
docker --version
```

#### Expected Result

Docker should print the installed version.

#### Notes

Docker is required to run the Doosan emulator.

---

### Check Docker access without sudo

#### Purpose

Verify that Docker can be executed without using `sudo`.

#### Command

```bash
docker ps
```

#### Expected Result

Docker should list running containers or show an empty list.

#### Notes

If this command fails with a permission error, the user may not be correctly added to the `docker` group.

---

## ROS 2 Commands

### Check active ROS 2 distribution

#### Purpose

Verify which ROS 2 distribution is currently active in the terminal.

#### Command

```bash
echo $ROS_DISTRO
```

#### Expected Result

```text
jazzy
```

#### Notes

If the output is empty, ROS 2 has not been sourced in the current terminal.

---

### List available ROS 2 services

#### Purpose

List available ROS 2 services in the current ROS graph.

#### Command

```bash
ros2 service list
```

#### Expected Result

ROS 2 should print the services currently available.

#### Notes

This command is useful to confirm that the Doosan controller services are visible.

---

## Doosan ROS 2 Commands

### Check MoveJoint service type

#### Purpose

Verify the service type used by the Doosan joint motion service.

#### Command

```bash
ros2 service type /dsr01/dsr_controller2/motion/move_joint
```

#### Expected Result

```text
dsr_msgs2/srv/MoveJoint
```

#### Notes

This confirms that the `move_joint` service is available and uses the expected Doosan service interface.

---

### Inspect MoveJoint service definition

#### Purpose

Inspect the request and response fields required by the `MoveJoint` service.

#### Command

```bash
ros2 interface show dsr_msgs2/srv/MoveJoint
```

#### Expected Result

ROS 2 should print the full service definition for `dsr_msgs2/srv/MoveJoint`.

#### Notes

This command is important before writing any Python client with `rclpy`.

---

## Pending Commands to Document

The following commands still need to be documented after they are tested again:

- command to launch the Doosan emulator;
- command to launch RViz2 with the Doosan `m1013`;
- command to launch MoveIt2;
- command to launch Gazebo;
- command to call `/dsr01/dsr_controller2/motion/move_joint`;
- command to list Doosan-related services only;
- command to inspect available `dsr_msgs2` interfaces.

---

## Command Documentation Template

Use this template when adding new commands:

```md
### Command title

#### Purpose

Explain what the command does.

#### Command

```bash
command_here
```

#### Expected Result

Describe the expected output or behavior.

#### Notes

Add any relevant context, warning, or requirement.
```