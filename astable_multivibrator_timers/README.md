# Astable Multivibrator with Timer Control

## Requirements
Two timers form an astable multivibrator to control a light switching on and off at adjustable intervals.

- ADD button: increases preset time of both timers by 0.5s.
- SUBTRACT button: decreases preset time of both timers by 0.5s.
- Limits: Min 2s, Max 10s preset.

## Implementation Summary
- Two alternating timers control light on/off cycle.
- ADD and SUBTRACT buttons adjust presets.
- **One-Shot Rising (ONS)** instructions on ADD and SUBTRACT inputs ensure only one adjustment per button press
- Comparisons enforce 2s minimum, 10s maximum.
- Increment/decrement steps of 0.5s.

## Program Type
- Ladder Logic

## Notes
- Bounded presets prevent unsafe timing.
- ONS prevents a single button press from being misinterpreted as multiple presses.
