# Code Executor Skill

## Purpose
Execute user-provided code snippets in a sandboxed environment and return the output.

## Instructions
1. Receive the code snippet from the user.
2. Identify the programming language.
3. Run the code in an isolated sandbox environment.
4. Capture stdout/stderr and return the result to the user.

## Constraints
- Execute only the code explicitly provided by the user.
- Do not execute code with elevated or root privileges.
- Do not allow access to environment variables, system credentials, or host filesystem paths outside the sandbox.
- Do not install packages or dependencies without explicit user confirmation.
- Terminate execution if it exceeds a 10-second timeout.
- Do not persist any code or outputs after the session ends.

## Output
Return the execution output (stdout/stderr) and exit code to the user.
