# `pallet_layout_core` Implementation Notes

## Purpose

This module generates robot-agnostic pallet layouts, layers, slots, and target poses.

## Scope

This module is responsible for:

- Box dimensions.
- Pallet dimensions.
- Layer generation.
- Slot generation.
- Target pose calculation.
- JSON export.

This module is not responsible for:

- ROS 2 node execution.
- Doosan service calls.
- MoveIt2 planning.
- Gazebo simulation.
- Robot kinematics.
- Dashboard UI.

## Coordinate Convention

- The pallet origin is located at the lower-left corner of the pallet footprint.
- X follows the pallet length.
- Y follows the pallet width.
- Z follows the pallet height.
- Slot positions represent the geometric center of each box.

## Initial Position Formula

```text
x = box.length / 2 + column_index * box.length
y = box.width / 2 + row_index * box.width
z = pallet.height + box.height / 2 + layer_index * box.height
```

## Initial Supported Pattern

Only the `grid` pattern is supported in the first version.

## Known Limitations

- Only rectangular pallets are supported.
- Only one box type is supported.
- Only one orientation is supported initially.
- No collision checking is performed.
- No robot reachability validation is performed.
- No trajectory generation is performed.
