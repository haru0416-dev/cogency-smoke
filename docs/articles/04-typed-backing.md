# Article IV: Typed backing

Backing references must be typed.

Bare links or vague prose do not count as backing.

Allowed forms:

- `observation:<path>:<line-range>`
- `comparison:<CR-id>`
- `claim:<CR-id>`
- `artifact:<path>`
- `external:<namespace>:<id-or-url>`

Examples: `external:arxiv:2604.02485`, `external:beads:bd-c4d2`, `external:repo:tokio-rs/tokio`.

Source authority is not claim correctness.

For version-sensitive external claims, `external:` backing must be paired with a local anchor, source quality, version fit, and stale-risk note before it can support `confirmed`.
