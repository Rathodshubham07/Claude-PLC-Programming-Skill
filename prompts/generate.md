# PLC Code Generation Prompt

Before generating vendor-specific PLC code, identify the target PLC, CPU/family, engineering software/version and language.

Then:

1. Restate the requirement.
2. List assumptions.
3. Define inputs and outputs.
4. Define operating modes.
5. Define permissives and interlocks.
6. Define faults and reset behavior.
7. Define sequence/state machine where appropriate.
8. Generate platform-specific code.
9. Explain the code.
10. Provide validation checks and test cases.

Do not invent hardware addresses, vendor instructions, timer semantics or unsupported features.