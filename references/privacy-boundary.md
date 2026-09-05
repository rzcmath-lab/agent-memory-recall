# Privacy and Public-Release Boundary

Memory systems are likely to contain sensitive user and organizational information. Retrieval permission is not publication permission.

## Never publish

- Raw conversations, logs, traces, screenshots, prompts, or tool payloads
- Names, emails, phone numbers, account IDs, session IDs, repository paths, device paths, IP addresses, or private domains
- Credentials, API keys, tokens, cookies, certificates, environment values, or connection strings
- Employer-specific service names, internal architecture, business rules, field names, thresholds, incidents, or metrics
- Customer, employee, operational, financial, medical, or other personal data

## Safe public transformation

1. Extract only the general engineering decision.
2. Replace every actor, identifier, path, record, and example with synthetic content.
3. Remove proprietary terminology and implementation-specific constants.
4. Present architecture at the responsibility and trust-boundary level.
5. Run deterministic secret, identifier, and path scans.
6. Require human approval immediately before publication.

This repository publishes design documentation only. It does not grant permission to export any underlying memory store or implementation.
