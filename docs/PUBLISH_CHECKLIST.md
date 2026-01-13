# Publish Checklist

## Included

- `README.md`
- `docs/PAPER_PUBLISH_READY.md`
- `docs/CHANGELOG.md`
- `docs/SUBMISSION_TODO.md`
- `docs/METHODS_EXTRACTED_PUBLIC.md`
- `docs/PUBLIC_RELEASE_NOTES.md`
- `docs/SECURITY_AND_PRIVACY.md`
- `/evidence` bundle (redacted) with `README.md` and `SHA256SUMS.txt`
- `LICENSE`, `CITATION.cff`, `.gitignore`

## Intentionally Excluded

- Source code, tests, and internal specs (`src/`, `tests/`, `spec/`).
- Unlock tokens, hidden subset identifiers, and any private workspace paths.

## Remaining TODOs (from `docs/SUBMISSION_TODO.md`)

- Environment fingerprint for reported runs.
- Exact install steps and lockfile/constraints.
- Determinism incident handling beyond `CMD-013`.
- Guidance on DI50 comparability across snapshots/iterations.
- RLVR objective, training algorithm, and hyperparameters.
- PEFT training details beyond adapter config.
- Compute budget and runtime details for reported iterations.
- Formal citations for verifier-based learning, DI/IRT, PEFT, and RLVR-related work.
- Final decision on what artifacts will be publicly released (beyond this docs-only bundle).
