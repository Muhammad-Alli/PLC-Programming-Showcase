# Hazardous Gas Safety System (Fail-Safe)

## Requirements
Monitor hazardous gas levels and trigger alerts/actions:

- gas_low: Healthy indication active.
- gas_medium: Warning alarm ON, exhaust fans ON, air pump ON.
- gas_high: Emergency alarm ON, trip signal to shut down machinery, close adjacent zone doors.

## Implementation Summary
- Inputs `gas_low`, `gas_medium`, `gas_high` drive separate logic branches.
-Low gas level: activates healthy gas indication.
- Medium gas level: activates warning, fans and pump operated for 10 seconds.
- High gas level: emergency shutdowns and door closure.
- Master reset logic only active when `gas_high` is off.

## Program Type
- Ladder Logic

## Notes
- Built to fail-safe principles to protect personnel in hazardous environments:
    - Master reset button only works if gas_high is inactive.
    - Master reset button prevents sudden automatic restart of equipment when gas levels drop below gas_high.
-The addition of a timer, to control the medium gas level operations, is necessary to prevent the system from oscillating between the medium and low gas threshold states
