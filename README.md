# `.github` — organization defaults

This repository holds no tracker code. It carries the files GitHub serves as the **default for
every repository in [satoshi-onchain](https://github.com/satoshi-onchain)** that does not ship its
own. If you arrived here from a policy link on another repository, this is why.

| File | What it says |
| --- | --- |
| [`SECURITY.md`](SECURITY.md) | The boundary this project is built on: the Patoshi cluster is a **fingerprint, not a signature**. "You cannot prove these blocks are Satoshi's" is correct, and is already the project's own position. What *is* in scope, and how to report it. |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to send a change, and the three evidence tiers a claim can sit at. |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Contributor Covenant, plus what counts as evidence here. |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | The two reports worth structuring: a figure that does not re-derive, and a claim graded above its tier. |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Asks a changed figure to arrive with its re-derivation. |
| [`profile/README.md`](profile/README.md) | The organization landing page. |

A repository that ships its own copy of any of these overrides the default. That is the intended
way to specialize: override the file, do not weaken the default.

## The tracker

**[`satoshi-onchain`](https://github.com/satoshi-onchain/satoshi-onchain)** — a reproducible
Satoshi/Patoshi on-chain tracker. Every figure re-derives from public chain data with a published
command. Everything is graded **[forensic]**, never **[cryptographic]**; no verifying signature
exists, and none is claimed.

Site: <https://satoshioncha.in>
