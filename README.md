# Claude PLC Programming Skill

A vendor-aware PLC programming engineering skill for Claude and other AI assistants.

## Purpose

This project teaches an AI assistant to work like a disciplined industrial automation engineer: understand the control requirement, identify the PLC platform, design the sequence and interfaces, generate appropriate PLC logic, review it for faults and edge cases, and provide validation tests.

## Core capabilities

- PLC architecture and scan-cycle reasoning
- IEC 61131-3 concepts
- Ladder Diagram (LD)
- Structured Text (ST)
- Function Block Diagram (FBD)
- Sequential Function Chart (SFC)
- State-machine design
- Motor, pump, valve and conveyor control
- Auto/manual/semi-auto/simulation modes
- Permissives and interlocks
- Alarm and fault management
- Timers, counters and edge detection
- Analog scaling and instrumentation
- Sequence control
- Code review and troubleshooting
- HMI/SCADA interface considerations
- Simulation and test-case design

## Vendor-aware design

The skill is intentionally structured so generic IEC principles are separated from vendor-specific behavior. The assistant must identify the target PLC, engineering software and version before producing vendor-specific code.

Initial vendor areas:

- Siemens TIA Portal / S7
- Rockwell Automation Studio 5000 / Logix
- Mitsubishi GX Works
- Schneider EcoStruxure / Modicon
- Generic IEC 61131-3

## Engineering workflow

```text
Requirement
    -> Platform identification
    -> I/O definition
    -> Operating modes
    -> Sequence / state machine
    -> Permissives
    -> Interlocks
    -> Faults / alarms
    -> PLC implementation
    -> Logic review
    -> Test cases
    -> Simulation / compilation / commissioning
```

## Important safety notice

This is an engineering-assistance project. Generated PLC code is not safety-certified and must be reviewed, tested and validated by qualified automation and safety personnel before deployment on real equipment.

The skill must never invent vendor-specific instructions or claim that uncompiled code has been compile-validated.

## Repository structure

- `SKILL.md` — master skill instructions
- `docs/` — engineering methodology
- `standards/` — IEC and PLC fundamentals
- `vendors/` — vendor-specific guidance
- `patterns/` — reusable control patterns
- `examples/` — reference implementations
- `tests/` — evaluation scenarios
- `prompts/` — task-specific prompt templates

## Status

Version 0.1.0 — foundational PLC engineering skill.

## License

MIT License. See `LICENSE`.
