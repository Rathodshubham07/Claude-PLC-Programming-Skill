# PLC Logic Validation

Generated PLC code must be evaluated at the highest level actually performed.

## Validation levels

1. Requirement review
2. Logical/static review
3. Vendor syntax review
4. Actual compilation
5. Simulation
6. Hardware-in-the-loop
7. Commissioning

Never report a higher level than was actually completed.

## Minimum review checklist

- [ ] Correct PLC platform and version identified
- [ ] Inputs and outputs defined
- [ ] Modes defined
- [ ] Permissives defined
- [ ] Interlocks defined
- [ ] Faults defined
- [ ] Reset behavior defined
- [ ] Timer behavior reviewed
- [ ] Counter behavior reviewed
- [ ] State transitions reviewed
- [ ] Conflicting output writes checked
- [ ] Scan-cycle implications reviewed
- [ ] Boundary conditions tested
- [ ] Abnormal conditions tested
- [ ] Recovery behavior tested
- [ ] Safety architecture kept separate from ordinary control logic

## Test categories

Normal operation, boundary conditions, abnormal conditions, reset/recovery, mode changes, conflicting commands and restart/power-cycle behavior where applicable.