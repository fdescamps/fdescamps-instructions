# Ping Pong Programming (AI & Programmer Roles)

## Sequence of steps
1. The programmer writes a failing test.
2. The AI (Copilot) makes the test pass in the simplest way possible.
3. The AI (Copilot) refactors the code to improve it, if needed.
4. The AI (Copilot) updates the specification file to reflect that the test has passed.
5. The AI (Copilot) writes the next failing test.
6. The programmer makes the new test pass in the simplest way possible.
7. The programmer refactors the code to improve it, if needed.
8. The programmer updates the specification file to reflect that the test has passed.
9. Repeat steps 2–6, alternating roles, until the feature is complete.

## Rules
Only one failing test should be added at a time.
Each participant (AI or programmer) only does their assigned steps before handing off.
Refactoring should be done after making a test pass, before writing the next test.
The specification file should be updated after a test passes to reflect the current state of the feature.
We code in javascript
