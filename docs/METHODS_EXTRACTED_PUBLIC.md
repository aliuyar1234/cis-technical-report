# Methods Extracted (Public Summary)

This document summarizes method facts that are already described in the paper. Implementation code and private specs are intentionally withheld in this docs-only release.

- Deterministic seeding and execution contract for evaluation/training, including explicit `--deterministic` mode and seed recording. Evidence: Paper Section 8.2.
- Config hashing via SHA-256 of resolved canonical JSON. Evidence: Paper Section 8.2.
- Artifact content-addressing with SHA-256 over canonical JSON and immutable run records. Evidence: Paper Sections 3.2 and 4.2.
- PASS@1 evaluation semantics (`attempt_index=0`, deterministic verifiers, visible subset only). Evidence: Paper Section 3.3 and Section 5.4.
- Decoding behavior and attempt budgeting (greedy at `attempt_index=0`, budgets from `BUDGET-001`, capped for certain families). Evidence: Paper Section 3.3.
- Suite snapshots with hidden subsets and sealed evaluator mode with explicit unlock. Evidence: Paper Section 4.3 and Section 5.2.
- DI calibration model (1PL logistic / Rasch-style MAP), DI50 and CI95 definitions, and stability checks. Evidence: Paper Section 3.4.
- Sandbox offline-by-default enforcement, incident recording on violations. Evidence: Paper Section 4.4 and Section 8.2.
- Promotion/rollback gates and never-worse regression policy. Evidence: Paper Section 4.7 and Section 6.3.
- RLVR dataset construction from verifier-based rewards and group-standardized advantages. Evidence: Paper Section 4.6.
- Dependency manifest for runtime and sandbox pins. Evidence: Paper Section 8.1.1.
- CLI help output captured for the canonical command surface. Evidence: Paper Appendix A.1.

Internal implementation references are available upon request; public evidence artifacts (when available) are provided under `/evidence`.
