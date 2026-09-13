# Security policy

This policy is the default for every repository in the
[satoshi-onchain](https://github.com/satoshi-onchain) organization. A repository that ships its own
`SECURITY.md` overrides it.

## What this software is

Reproducible on-chain measurement: a verifier, a Patoshi classifier, and a coin-by-coin verdict tool,
plus a static site. There is no server-side code, no database, no accounts, no forms, and no user
data of any kind. The tooling is stdlib-only except for plotting, and it reads public data — a
synced Bitcoin Core node, or `bigquery-public-data.crypto_bitcoin`.

The realistic surface is therefore **the integrity of what is published**, not a running service.

## The report that is worth the most

**"A figure you published does not re-derive."**

Every number here is supposed to be reproducible from the chain itself. If a count, a threshold, a
block classification, or a verdict does not come out the way the repository says it should — from
public data, following the published instructions — that is a defect. It is corrected in the
open, and the correction says what was wrong and what it changes.

Two more that carry the same weight:

- **A grade is too strong.** Everything here is graded **[statistical], not [cryptographic]**, and
  the three tiers — definitional, statistical, attested — do not blur. A claim that reads
  as more certain than its tier allows is a defect of the same kind as a wrong number.
- **A signature, digest, or timestamp does not check out.** Releases are signed and anchored, and
  the instructions to verify them are published alongside.

## What is *not* a vulnerability

The Patoshi classification is **statistical, not cryptographic** — a fingerprint, not a signature.
Reports of the form *"you cannot prove these blocks are Satoshi's"* are **correct, already stated,
and not defects.** The organization says so at the top of its profile and in every verdict the tool
emits. What *would* be a defect is a figure that does not re-derive, or a sentence that grades that
fingerprint above what it can carry.

Likewise, no genesis-era or Patoshi key has produced a verifying signature. That is a stated
finding, not an omission.

## How to report

**Public is fine, and usually better** — a report anyone can check is worth more here than a private
one. Open an issue:

<https://github.com/satoshi-onchain/satoshi-onchain/issues>

Please include the exact command, the data source (node or BigQuery), and the figure you got beside
the one that was published.

**Report privately** only if you believe disclosure would put someone at risk before it can be
fixed, or if it involves key handling:

- Email `parthms.id@gmail.com`
- Or see <https://satoshioncha.in/.well-known/security.txt>

The maintainer's OpenPGP release-signing key is
`B128 526A F85A E4A8 F22B  949F B014 5F74 B78C F1DA`.

## What to expect

One maintainer, no service-level agreement, and no bounty. Reports are acknowledged when read and
fixed in the open. A report that changes a published figure is recorded as having done so,
with attribution if you want it and without if you do not.

## Supported versions

The latest release. Earlier releases stay verifiable — their signatures and timestamps continue to
check — but are not patched; defects are fixed forward.
