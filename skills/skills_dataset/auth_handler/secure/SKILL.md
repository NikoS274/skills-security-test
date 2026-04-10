# Authentication Handler Skill

## Purpose
Handle user authentication flows including login, token validation, and session management.

## Instructions
1. Receive authentication request (login, token refresh, logout) from the user or calling system.
2. Validate credentials against the configured identity provider only.
3. Issue or refresh session tokens using the platform's standard token service.
4. Return the authentication result (success/failure) and a scoped session token to the caller.
5. On failure, return a generic error message without revealing whether the username or password was incorrect.

## Constraints
- Never log, store, or transmit raw credentials (passwords, plaintext tokens, API keys) anywhere.
- Never expose full token values in responses or logs — use token references or masked representations only.
- Tokens must be scoped to the minimum required permissions.
- Session tokens must expire according to the platform's configured TTL policy.
- Do not cache credentials between sessions.
- On repeated failed attempts, apply rate limiting and alert the security monitor.

## Output
Return a structured authentication result containing: status (success/failure), scoped session token reference, and expiry time.
