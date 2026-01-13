# CIS: A Deterministic, Offline-by-Default Compounding Intelligence Sandbox with Verifier-Gated Self-Improvement

CIS (Compounding Intelligence Sandbox) is an offline-by-default, determinism-first system for verifier-grounded capability growth on verifiable tasks, with immutable run records and promotion/rollback gating for regressions.

## Results Snapshot

PASS@1 on visible tasks (baseline vs. champion):

| Suite | Baseline PASS@1 (iter-000021) | Champion PASS@1 (iter-000149) |
| --- | ---: | ---: |
| `core_code` | 0.0000 | 1.0000 |
| `core_math` | 0.1250 | 1.0000 |
| `core_logic` | 0.5000 | 0.8077 |
| `concept_understanding` | 0.0000 | 1.0000 |

DI50 (iter-000149): **2.2083** with **CI95** **[1.7033, 2.7133]**.

## What's Public vs. Private

- Public: paper (`docs/PAPER.md`), supporting docs, and a redacted evidence bundle under `/evidence`.
- Private: implementation code and internal specs.

Docs overview: `docs/INDEX.md`.

## How to Verify the Claims (No Training Required)

1. Read the paper in `docs/PAPER.md` for methodology and reported results.
2. Inspect `/evidence/README.md` for the list of included redacted artifacts and redaction policy.
3. Cross-check the PASS@1 table and DI50/CI95 values against the evidence files (when available).

## Evidence Verification (Quick Checks)

- Compare PASS@1 values in `evidence/reports/iter-000021/metrics.json` and `evidence/reports/iter-000149/metrics.json` against the table above.
- Confirm DI50/CI95 in `evidence/reports/iter-000149/summary.md` matches the value stated in the paper and README.
- Verify run IDs and seeds in `evidence/runs/*/run_record.json` match the IDs cited in the paper.

For release details and redaction policy, see `docs/PUBLIC_RELEASE_NOTES.md` and `docs/SECURITY_AND_PRIVACY.md`.
