# Conveyor Control Pattern

A conveyor control module should normally separate command, permissives, interlocks, feedback, faults and status.

## Typical signals

Inputs:

- Start command
- Stop command
- Auto enable
- Manual command
- Motor running feedback
- Overload/fault feedback
- Safety/permissive status
- Entry sensor
- Exit sensor
- Reset command

Outputs:

- Motor command
- Fault/status indicators

## Typical sequence

1. Verify permissives.
2. Verify no active blocking fault.
3. Accept manual or automatic command according to mode.
4. Issue motor command.
5. Monitor running feedback.
6. Start timeout if feedback is not received within the defined limit.
7. Stop according to command or sequence.
8. Monitor stop feedback when required.
9. Latch and report defined faults.
10. Permit recovery only through the specified reset/recovery process.

## Design notes

Do not assume that an emergency stop is implemented by ordinary PLC logic. Use the actual safety architecture.

The exact timer instruction, tag syntax and implementation depend on the PLC platform.