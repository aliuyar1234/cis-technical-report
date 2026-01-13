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

## Verification Mapping (where reported numbers live)

- PASS@1 (baseline): `reports/iter-000021/metrics.json` → `pass_at_1`.
- PASS@1 (champion): `reports/iter-000149/metrics.json` → `pass_at_1`.
- DI50/CI95: `reports/iter-000149/metrics.json` → `di50`, `di50_ci95_low`, `di50_ci95_high` (also summarized in `reports/iter-000149/summary.md`).
- Cited promotion run/seed: `runs/run-20260112T124809Z-d74cd05c/run_record.json` → `run_id`, `seed`, `model_selector.adapter_id`.
- Cited rollback runs/seeds: `runs/run-20260112T131450Z-ec2875b8/run_record.json`, `runs/run-20260112T142709Z-9477cd3c/run_record.json`.

## Redaction Policy

Evidence artifacts in this folder are redacted to remove:

- Local absolute paths, usernames, machine identifiers, and environment fingerprints.
- Unlock tokens and any hidden subset identifiers.

Run IDs, iteration IDs, adapter IDs, seeds, and PASS@1/DI50/CI95 values will remain unchanged.

Redaction notes:
- `run_record.json` files have `git.commit`, `workspace_id`, and `schema_hash` set to `REDACTED`.
- Summary links normalize Windows path separators to forward slashes.
