# Test: Sequence State Machine

## Objective

Evaluate whether the assistant designs explicit and testable sequence states.

## Required behavior

```text
IDLE → STARTING → RUNNING → STOPPING → IDLE
             \→ FAULT ←/
```

## Evaluation criteria

- States are explicit.
- Transitions have clear conditions.
- Entry and exit behavior is defined.
- Timeout behavior is defined.
- Fault behavior is defined.
- Reset behavior is defined.
- Invalid transitions are considered.
- Mode changes are considered.
- Required feedback is monitored.

A good answer should not hide the sequence entirely inside unrelated Boolean latches.