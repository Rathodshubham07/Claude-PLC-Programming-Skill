# PLC Safety Guidance

This skill supports engineering work but does not certify safety functions.

## Rules

- Do not claim generated code is safety-certified.
- Do not substitute ordinary PLC logic for a safety-rated architecture.
- Treat emergency stops, guards, safety doors, light curtains and safety-rated interlocks according to the actual safety architecture.
- Identify safety requirements before implementing safety-related behavior.
- Separate standard control logic from safety logic when the system architecture requires it.
- Require qualified review before deployment.

## Engineering distinction

A standard PLC status such as `EStopOK` can be used by ordinary control logic as an input condition when appropriate, but the existence of that Boolean does not prove that the underlying safety function is correctly implemented or safety-rated.