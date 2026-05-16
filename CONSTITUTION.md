# Cogency Constitution

This file summarizes the constitutional Articles Cogency installs into AI-written codebases.

During the design-first phase, this file is the resident Article summary. The canonical implementation-phase Article text will live under `docs/articles/`. This summary is intentionally short enough to fit in an agent's resident context.

## Article I: UNKNOWN — probe

Unknown is a valid state, not a failure. If a claim cannot be justified, the record must say `unknown` and name the probe that would reduce uncertainty.

No `Why` is valid without one of: direct evidence, calibrated reasoning marked `plausible`, or `UNKNOWN — probe: <next step>`.

## Article II: Disconfirming probe

Every Claim Record must include at least one disconfirming probe. Each disconfirming probe has four required fields:

- `target`: where the claim would break;
- `method`: how that target was checked;
- `result`: what the check found;
- `limitation`: what the check did not cover.

`none`, `n/a`, `tbd`, and equivalent placeholders are not acceptable limitations.

## Article III: Decision states

Decision state is explicit and finite:

- `proposed`
- `confirmed`
- `inconclusive`
- `rejected`
- `superseded`

`confirmed` with `confidence: unknown` is invalid. An inconclusive result is a legitimate endpoint.

## Article IV: Typed backing

Backing references must be typed. Bare links or vague prose do not count as backing.

Allowed forms:

- `observation:<path>:<line-range>`
- `comparison:<CR-id>`
- `claim:<CR-id>`
- `artifact:<path>`
- `external:<namespace>:<id-or-url>`

Examples: `external:arxiv:2604.02485`, `external:beads:bd-c4d2`, `external:repo:tokio-rs/tokio`.

Source authority is not claim correctness. For version-sensitive external claims, `external:` backing must be paired with a local anchor, source quality, version fit, and stale-risk note before it can support `confirmed`.

## Article V: Scope and staleness

Every Claim Record must define scope and staleness.

Scope says what the claim covers and what it does not cover. Staleness says what kind of change makes the claim suspect again: code change, dependency change, spec change, or manual review.

Scope is a claim, not decoration. If a record cannot say what is out of scope, it is not ready to promote.
