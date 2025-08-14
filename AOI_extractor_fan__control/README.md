# Air Extractor Fan Motor Control

## Requirements
Design a STOP / START control for a large air extractor fan motor:
- Use I/O simulator contacts for START (N/O) & STOP (N/O).
- Motor cannot be started again for 10 seconds after stopping.
- Limit starts to 5; after the 5th start, a flashing light warns service is due.
- After the 5th stop, light stays solid to indicate service is required before next run.
- Maintenance reset is done with a key-switch after servicing.

## Implementation Summary
- Two N/O push buttons for START and STOP.
- 10-second off-delay timer to prevent restarts immediately after stopping.
- Counter to track motor starts.
- Comparison logic to stop the motor after 5 starts.
- Flashing light circuit for 5th run, steady-on light after final stop.
- Keyed maintenance reset to clear counter and light after service.

## Program Type
- Ladder Logic

## Notes
- Cooldown and start limit logic protect motor longevity.
- Maintenance lockout ensures service before restart.
