# PLC Code Review Prompt

Use this prompt when reviewing PLC code.

## Required input

Ask for the PLC manufacturer, CPU/family, engineering software/version and programming language if they are not known.

## Review process

1. Explain what the existing code appears to do.
2. Compare it against the stated requirement.
3. Identify syntax/platform concerns.
4. Check scan-cycle behavior.
5. Check state/latch behavior.
6. Check timers and counters.
7. Check permissives and interlocks.
8. Check fault and reset behavior.
9. Check operating modes.
10. Check duplicate/conflicting output writes.
11. Check edge cases.
12. Rank findings by severity.
13. Provide corrected code only where needed.
14. Provide test cases for each important finding.

Never claim that code compiles unless it was actually compiled in the target environment.