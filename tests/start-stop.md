# Test: Start/Stop Equipment

## Objective

Verify that a generic motor-style equipment module responds correctly to commands and permissives.

## Preconditions

- Safety/permissive condition healthy
- No blocking fault
- Equipment in the intended operating mode

## Test cases

| Test | Condition | Expected result |
|---|---|---|
| 1 | Start command + permissive healthy | Start command is issued |
| 2 | Stop command active | Start command is removed |
| 3 | Start command + permissive false | Equipment does not start |
| 4 | Running feedback absent during start | Defined start timeout fault occurs |
| 5 | Fault active | Equipment remains in defined safe/controlled state |
| 6 | Reset while fault condition remains | Fault does not incorrectly clear |
| 7 | Fault cleared + valid reset | Fault clears if reset criteria are satisfied |
| 8 | Manual/Auto transition | Behavior matches documented mode strategy |

The exact implementation and timer behavior must be evaluated for the target PLC platform.