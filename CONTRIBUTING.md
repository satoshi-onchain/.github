# Contributing

This is the default for every repository in the
[satoshi-onchain](https://github.com/satoshi-onchain) organization. A repository that ships its own
overrides it.

Thanks for your interest. This organization answers one question — *what is the verifiable on-chain
footprint of the original Satoshi on the original Bitcoin chain* — and it answers it only from data
anyone can re-derive.

## The two rules that matter

**1. Every figure must re-derive from public data.** A synced Bitcoin Core node, or
`bigquery-public-data.crypto_bitcoin`. A number that cannot be recomputed by a stranger following
published instructions does not belong here, however plausible it is.

**2. Nothing is graded above what the evidence supports.** The three tiers are kept separate and
never blurred:

| Tier | What | Certainty |
|---|---|---|
| **A · Definitional** | The genesis block: its coinbase message, key, and unspendable 50 BTC, hardcoded in consensus. | Certain |
| **B · Statistical** | The Patoshi cluster, fingerprinted by block-header structure. | Statistical, not cryptographic |
| **C · Attested** | Block 170, Satoshi → Hal Finney. | On-chain certain that the spend happened; the attribution rests on B plus Finney's account |

A contribution that moves a claim up a tier needs the evidence for that tier. Nothing here is
**[cryptographic]** unless a key has produced a verifying signature, and none has.

## Reporting issues and asking questions

Open an issue: <https://github.com/satoshi-onchain/satoshi-onchain/issues>

For a figure that does not reproduce, include the exact command, the data source, and the number you
got beside the published one. Disclosure can be public; see [`SECURITY.md`](SECURITY.md) for the
narrow cases where it should not be.

## What is out of scope

- **Identity claims.** Asserting that a particular person is or is not Satoshi is not evidence,
  in either direction, and the issue tracker is not the place for it.
- **Off-chain sources** as the basis for an on-chain claim. Forum posts, emails, and interviews may
  be cited as context; they cannot upgrade a grade.
- **Speculation about living people.**

## Pull requests

1. Branch from `main` and keep changes focused.
2. Add or update tests for any behavior change.
3. A change to a published figure must show the re-derivation — the command and its output.
4. A change to a claim's wording must not raise its grade without the evidence that tier requires.
5. Keep the tooling stdlib-only except for plotting; a new dependency needs a reason in the PR.

## Attribution and licensing

By contributing you agree that your contribution is licensed under the repository's MIT license.
