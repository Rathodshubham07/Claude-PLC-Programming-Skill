# PLC State Machines

Use explicit state machines for equipment with meaningful sequential behavior.

## Recommended model

```text
IDLE → STARTING → RUNNING → STOPPING → IDLE
                    ↓
                  FAULT
```

## State definition

Each state should have:

- Entry behavior
- Active behavior
- Transition conditions
- Timeout handling
- Fault handling
- Exit behavior

## Rules

- Use explicit state identifiers.
- Define legal transitions.
- Avoid hidden state distributed across unrelated latches.
- Define reset behavior.
- Define what happens if a required feedback signal disappears.
- Define behavior when operating mode changes.
- Define timeout behavior for expected transitions.

The actual implementation must follow the target PLC platform's supported data types and programming conventions.