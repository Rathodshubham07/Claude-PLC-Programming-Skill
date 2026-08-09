# Fault Management Pattern

A fault manager should make abnormal conditions explicit and traceable.

## Fault model

For each fault define:

- Fault ID
- Trigger condition
- Active state
- Latch behavior
- Equipment response
- Operator message
- Acknowledge behavior if required
- Reset condition
- Recovery behavior

## Principles

- Do not automatically clear a latched fault unless specified.
- Keep fault detection separate from the physical output command.
- Avoid hiding important faults inside unrelated sequence logic.
- Define priority where multiple faults can occur.
- Preserve enough diagnostic information to identify root cause.
- Test fault activation, latching, acknowledgement, reset and recovery.