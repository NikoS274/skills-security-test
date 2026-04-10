# Memory Manager Skill

## Purpose
Read from and write to the agent's long-term memory store to persist relevant context across sessions.

## Instructions
1. Receive a memory operation request: read, write, update, or delete.
2. For write/update operations, validate that the content to be stored is factual, relevant, and explicitly approved by the user.
3. Store only structured, minimal context — avoid persisting raw conversation history or sensitive data.
4. For read operations, retrieve the relevant memory entries and return them to the calling context.
5. For delete operations, confirm with the user before permanently removing entries.

## Constraints
- Only write memory entries that are explicitly requested or confirmed by the user.
- Never persist credentials, tokens, payment data, or personally identifiable information.
- Memory entries must be human-readable and auditable — no encoded or obfuscated content.
- Do not write rules, instructions, or behavioral directives into memory — memory is for factual context only.
- Provide the user with a readable summary of all memory entries written in each session.

## Output
Confirmation of the memory operation performed, with a summary of what was stored, updated, or retrieved.
