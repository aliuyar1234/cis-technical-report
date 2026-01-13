# Changelog

**Source draft:** “PAPER_final.md” as provided in this chat.

## Major changes (publish-readiness)

1. **Re-structured into submission-grade sections** using the required headings (Abstract → Conclusion + Appendix).
2. **Path normalization:** replaced machine-specific absolute paths with a single convention:
   - Defined `WS_ROOT = <workspace_root>` once near the top.
   - Converted all workspace references to `<WS_ROOT>/...` with forward slashes.
3. **Terminology hardened and defined on first use:** CIS, verifier, verifiable task, artifact, run record, suite snapshot, hidden subset, sealed evaluator mode, deterministic mode, PASS@1, DI/DI50/CI95, promotion, rollback.
4. **Determinism contract expanded to reviewer-proof bullet points (10 bullets):**
   - Explicitly enumerated what is deterministic under `--deterministic`, seed semantics, attempt semantics (`attempt_index`), offline coupling, provenance capture, and TODO requirements for environment fingerprints and hashing specifics.
5. **DI50 section made defensible without guessing:**
   - Added interface-level definitions for DI/DI50/CI95 and explicitly marked missing statistical methodology as TODO (no invented estimator).
6. **Tables upgraded for clarity:**
   - Added captions and linked tables to the evaluation protocol (visible tasks only; verifiers; decoding TODO).
   - Ensured labels are unambiguous and consistent with the narrative.
7. **Contributions aligned with described content:**
   - Rewrote contributions to match what the draft actually specifies (no expansion beyond described system components and reported artifacts).
8. **Tone tightened to academic conservatism:**
   - Removed informal phrasing and strengthened falsifiability/traceability by referencing exact artifact locations (normalized under `<WS_ROOT>`).
9. **Added a Mermaid architecture diagram** consistent with the described components (CLI → run records/artifacts → sandbox → verifiers → reports → promotion/rollback + incidents).
10. **Inserted explicit TODO markers** wherever submission-grade detail is missing instead of guessing (environment, verifier specs, DI estimator, RLVR objective, decoding config, gate thresholds, sandbox implementation).

## Invariants preserved

- **All reported numbers** (PASS@1 values, DI50 and CI95, iter IDs, adapter IDs, seeds, run IDs) were preserved exactly.
- **All referenced file/path endpoints** were preserved in meaning; only formatting was normalized under `<WS_ROOT>/...`.
- **No new experiments, datasets, benchmarks, citations, or implementation details** were introduced beyond what is explicitly stated or directly implied by the draft.
