---
name: api-tester
description: Check a task-authorized API against its actual contract using permitted HTTP requests, response/content assertions, and relevant error cases.
---

# API Testing

Adapted from RightNow-AI/openfang. Retain the supplied MIT and Apache-2.0 notices. The package manifest records revisions and changes.

## Read the actual contract

Identify the allowed service, method/path, authentication if any, request fields, response shape, storage effects and important failures. If no formal specification exists, derive a small explicit contract from the approved requirements and current implementation. Do not build a specification service just to begin checks.

A task may require creating the application's own server API without an external API key. Do not assume an external provider, authentication, pagination, GraphQL or a paid account.

## Execute focused checks

- Use available permitted tools such as curl, a standard-library HTTP client or existing tests. curl/httpie/Postman/jq are examples, not installation requirements.
- Start with the required normal flow. Assert response status, relevant headers, body values/types and required storage effects; a 200 response alone is insufficient.
- Check consequential invalid inputs and missing resources. Expected status codes and behavior come from the actual contract; do not require a generic 400/401/403 for every API.
- Test authentication/roles, pagination, idempotency, CORS or GraphQL only if actually applicable. Do not probe remote schema/complexity or repeat mutations simply to complete a checklist.
- Respect documented bounded timeouts and retries. For an observed 429, follow the documented Retry-After when applicable; never induce rate limiting through rapid traffic.
- Test writes only when the task contract permits them, using appropriate disposable/local inputs. Preserve unrelated data. Do not call destructive production operations without authorization.

## Diagnose and report

For a failure, compare the actual method/path, documented authentication, safe request fields, response and storage behavior. A 4xx/5xx label is a clue, not proof of whose code is wrong. Ask diagnosing-bugs for important persistent failures when useful.

Use provided credentials only where allowed; keep secrets out of commands, scripts, logs and traces. Do not request personal model keys, connect another AI provider, change networks or automate the browser.

Record the actual request/check, safe relevant response, observed storage effect, contract mismatch and remaining gaps. Browser UI behavior requires a separate permitted manual check. Clean up only disposable data created by these checks.
