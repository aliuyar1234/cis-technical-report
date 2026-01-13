# Security and Privacy

This docs-only release is designed to protect sensitive artifacts while still allowing readers to evaluate reported results.

## Explicit Non-Disclosure

- Unlock tokens and any files that could grant sealed/hidden access are not published.
- Hidden subset task identifiers are not published.
- Local absolute paths, usernames, machine identifiers, and API keys/tokens are not published.

## Redaction Policy

Evidence artifacts, when included, are redacted to preserve:

- Run IDs, iteration IDs, adapter IDs, seeds, PASS@1 values, and DI50/CI95 values (unchanged).
- Removal of any local path, host/machine identifier, or credential-like content.

For a per-file summary of redactions, see `/evidence/README.md`.
