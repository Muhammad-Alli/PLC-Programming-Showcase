# Add-On Instruction: Factory Door Control

## Requirements
Create an AOI 'Open_Factory_Door':

- Triggered by forklift sensor 1m from door.
- Alarm and flashing light for 30s, then door opens (alarm stops, light stays ON).
- Limit switch detects full open, stops door motor.

## Implementation Summary
- Forklift sensor input activates AOI routine.
- AOI triggers alarm and flashing light via internal timer for 30 seconds.
- After timer expires, door motor output energizes to open door.
- Limit switch input stops motor, turns alarm off, and changes light to steady ON.
- Reset pushbutton in AOI resets sequence for next operation

## Program Type
- Ladder Logic / Add-On Instruction

## Notes
- Modular AOI adaptable for other door systems.
- A manual pushbutton to reset the AOI routine is included to demonstrate this functionality, highlighting that the same effect can be achieved automatically through downstream operations, which would normalize the routine for the next cycle.
