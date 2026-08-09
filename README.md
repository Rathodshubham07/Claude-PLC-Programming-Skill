# Claude PLC Programming Skill

A disciplined PLC engineering skill for Claude, focused on vendor-aware control logic, code generation, code review, troubleshooting, and validation.

## Scope

- IEC 61131-3 programming concepts
- Ladder Diagram, Structured Text, Function Block Diagram, SFC
- PLC scan-cycle and execution reasoning
- Equipment sequencing and state machines
- Manual / Auto / Semi-Auto / Simulation modes
- Permissives, interlocks, alarms and fault management
- Timers, counters, edge detection and analog scaling
- PLC code review and troubleshooting
- Test-case and validation design

## Vendor-aware by design

The skill does not assume that similar PLC platforms behave identically.

Before producing vendor-specific code, it requires the target platform to be identified, including the PLC family, CPU, engineering software/version and programming language where relevant.

Initial vendor targets:

- Siemens / TIA Portal
- Rockwell Automation / Studio 5000
- Mitsubishi / GX Works
- Schneider Electric / EcoStruxure
- Generic IEC 61131-3

Vendor-specific syntax, instructions, addressing and hardware behavior must be verified rather than guessed.

## Engineering workflow

```text
Requirement
    ↓
Platform identification
    ↓
I/O and data model
    ↓
Operating modes
    ↓
Sequence / state model
    ↓
Permissives and interlocks
    ↓
Faults and recovery
    ↓
PLC implementation
    ↓
Logic review
    ↓
Test cases
    ↓
Validation
```

## Design principles

1. Correctness over speed.
2. Never invent vendor-specific behavior.
3. Separate commands, permissives, interlocks, faults and status.
4. Prefer explicit state models for sequential equipment.
5. Treat PLC scan behavior as part of the logic.
6. Make reset and recovery behavior explicit.
7. Distinguish logical review from actual compilation, simulation and commissioning.
8. Keep safety-rated functions separate from ordinary control logic.

## Repository

```text
Claude-PLC-Programming-Skill/
├── SKILL.md      # Master instructions
├── README.md     # Project overview
└── LICENSE       # MIT License
```

The repository intentionally starts small. Detailed vendor modules, examples and automated evaluation suites should be added only when they contain verified, reusable engineering material.

## Usage

Use `SKILL.md` as the instruction set for Claude. For vendor-specific work, provide the exact PLC platform and version together with the engineering requirement and any existing project conventions.

## Safety

This project is an engineering assistant, not a safety-certified control system. Generated PLC logic must be reviewed, tested and approved by qualified personnel before deployment.

## License

MIT