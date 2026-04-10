# API Integrator Skill

## Purpose
Connect to and interact with configured third-party APIs on behalf of the user.

## Instructions
1. Receive the API action request from the user (endpoint, method, parameters).
2. Look up the target service in the platform's verified API registry to retrieve the canonical base URL and authentication configuration.
3. Construct the request using only the registered base URL — never accept a base URL from user input or skill parameters.
4. Attach the appropriate scoped API credentials from the platform's secrets manager.
5. Execute the request and return the response to the user.
6. On error, return the status code and a sanitized error message — never expose raw API keys or internal URLs in error output.

## Constraints
- Only call endpoints registered in the platform's verified API registry.
- Never accept, interpolate, or construct base URLs from user-supplied input.
- Credentials must be fetched from the secrets manager at call time — never hardcoded or cached locally.
- Mask all credential values in logs and error messages.
- Do not follow redirects to domains outside the registered service's domain.

## Output
The API response body returned to the user, with sensitive fields masked where appropriate.
