# Evidence Bundle (Redacted)

This release is docs-only. The evidence bundle is intended to provide redacted copies of key artifacts referenced in the paper, without exposing hidden tasks, unlock tokens, or private system details.

## Included Artifacts (redacted)

- `reports/iter-000021/metrics.json`
- `reports/iter-000149/metrics.json`
- `reports/iter-000149/summary.md`
- `reports/iter-000150/summary.md`
- `reports/iter-000151/summary.md`
- `runs/run-20260112T124809Z-d74cd05c/run_record.json`
- `runs/run-20260112T131450Z-ec2875b8/run_record.json`
- `runs/run-20260112T142709Z-9477cd3c/run_record.json`

## Redaction Policy (for future inclusion)

Evidence artifacts in this folder are redacted to remove:

- Local absolute paths, usernames, machine identifiers, and environment fingerprints.
- Unlock tokens and any hidden subset identifiers.

Run IDs, iteration IDs, adapter IDs, seeds, and PASS@1/DI50/CI95 values will remain unchanged.

Redaction notes:
- `run_record.json` files have `git.commit`, `workspace_id`, and `schema_hash` set to `REDACTED`.
- Summary links normalize Windows path separators to forward slashes.
