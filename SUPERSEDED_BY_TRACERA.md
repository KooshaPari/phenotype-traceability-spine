# SUPERSEDED — use Tracera instead

This repo (`KooshaPari/phenotype-traceability-spine`) is **superseded by
`KooshaPari/Tracera`** as the canonical home for the trace/PM domain.

## Why

The 2026-09-01 polyrepo audit found that this repo and Tracera held overlapping
concerns under three near-identical names (`tracera-core`, `tracely-core`,
`tracely-sentinel`). Tracera is the active superset; this repo's working
crates (`traceability-core`, `traceability-decorators`, `trace-gate`) are
subsumed by Tracera's runtime.

## What this means

- **Do not add new code here.** Bug fixes only.
- Tracera is now the canonical home for the PM/trace domain.
- This repo will be renamed to `zz-archive-phenotype-traceability-spine` after
  any open dependents are verified migrated (2026-10-01 target).

## Migration (for any dependents)

In `Cargo.toml`, replace:

```toml
traceability-core = { git = "https://github.com/KooshaPari/phenotype-traceability-spine" }
traceability-decorators = { git = "https://github.com/KooshaPari/phenotype-traceability-spine" }
trace-gate = { git = "https://github.com/KooshaPari/phenotype-traceability-spine" }
```

with Tracera workspace deps (verify exact crate names in Tracera's `Cargo.toml`).

## Audit

- Tier-3 P2 spec: `phenotype-registry/ecosystem-consolidation/dossier/TIER3-P2-TRACEABILITY-CLUSTER.md`
- SSOT: `phenotype-registry/registry/disposition-index.json` PR #541
