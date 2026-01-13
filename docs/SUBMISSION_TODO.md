# Submission TODO

This file enumerates submission-grade gaps that must be filled **without guessing** (i.e., by adding real documentation, schemas, and/or artifact evidence).

## A. Reproducibility and environment

- **TODO:** Provide full environment fingerprint for the reported runs:
  - OS + version
  - Python 3.11 patch version
  - GPU model(s)
  - Driver + CUDA versions (if applicable)
  - Key library versions (e.g., torch/transformers/peft/etc.)
  - Container image hash / runtime details (if sandbox uses containers)
- **TODO:** Document exact install steps and lockfile/constraints (dependencies are listed in `pyproject.toml`; sandbox pins in `docker/sandbox_base.Dockerfile`).

## B. Determinism contract (method-level completeness)

- **TODO:** Define determinism incident handling beyond CMD-013 (for example, incident reporting for ERR-001) and document criteria in the submission.

## E. DI calibration (DI, DI50, CI95)

- **TODO:** Provide guidance on comparability of DI50 across suite snapshots/iterations.

## F. Training loop: distillation + RLVR + PEFT

- **TODO:** Specify the RLVR objective and training algorithm:
  - Reward definition from verifiers
  - Any reward shaping or normalization
  - Losses used and how they combine with distillation
- **TODO:** Provide hyperparameters and training schedule:
  - Optimizer, learning rates, batch sizes, steps, gradient accumulation, etc.
  - Data mixture and sampling strategy
- **TODO:** Document PEFT training details beyond the reported adapter config:
  - Which parameters are trainable
  - Any constraints for LoRA/LoRA+/DoRA variants
- **TODO:** Provide compute budget and runtime details for the reported iterations.

## I. Related work and citations

- **TODO:** Add formal citations for:
  - verifier-based learning / unit-test verifiers
  - DI / difficulty estimation (IRT-style calibration)
  - PEFT methods (LoRA/LoRA+/DoRA)
  - any prior work explicitly relied on for RLVR framing

## J. Artifact availability / openness

- Public release decision (current):
  - This repository is a **docs-only** public release: paper + supporting docs + **redacted evidence** under `/evidence`.
  - Implementation code and internal specs are intentionally withheld.
  - Evidence includes redacted `metrics.json`, `summary.md`, and `run_record.json` files sufficient to verify the reported PASS@1 table and DI50/CI95 without running training.
  - License: see `LICENSE` (all rights reserved).
