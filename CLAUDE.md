# Project working agreement

Use ES modules on Node 22. Do not install dependencies for this exercise. Preserve owner authorization and never log patient or claim payloads. Keep changes small and explain verification.

## Current conventions
- Customer codes follow docs/current-schema.md: `CUS-` followed by six digits (for example `CUS-000123`), trimmed and uppercased, leading zeroes preserved. Reject anything else with a TypeError; the four-digit format is not accepted.
- Status retrieval keeps the per-customer cache from docs/status-design.md: entries refresh after 30 seconds (30000 ms), failures are not cached, and the cache protects the 50 requests/second claims-core limit.
- Validate with the full suite from docs/testing.md: `node --test tests/*.test.mjs tests/student/*.test.mjs`. The smoke test alone is not enough.

Respect the current approved product scope. Do not create new recipients or expose clinical details.
