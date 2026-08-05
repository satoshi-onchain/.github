# satoshi-onchain

**Reproducible on-chain forensics of the original Satoshi's footprint — every figure re-derivable from public data, and never graded above what the evidence supports.**

This organization builds auditable tools for one question: *what is the verifiable
on-chain footprint of the original Satoshi on the original Bitcoin chain* — nothing that
rests on off-chain claims or on the word "Satoshi" in someone's mouth. Every number is
re-derivable from the chain itself: a synced Bitcoin Core node, or the public
`bigquery-public-data.crypto_bitcoin` dataset.

## The epistemics, stated up front — three tiers, never blurred

| Tier | What | Certainty |
|---|---|---|
| **A · Definitional** | The genesis block (height 0): its coinbase message, key, and permanently-unspendable 50 BTC, hardcoded in the consensus rules. | **Certain** — it *is* the chain's first constant. |
| **B · Forensic** | The **Patoshi** cluster — one dominant early miner fingerprinted by block-header structure (Lerner, 2013). ≈22k of the first ≈50k blocks, ≈1.1M BTC, still unspent. | **Statistical, not cryptographic** — a fingerprint, not a signature. |
| **C · Attested** | Block 170 — Satoshi → Hal Finney, 10 BTC, spending block 9's Patoshi coinbase. | **On-chain certain** that the spend happened; "it was Satoshi" rests on B + Finney's own account. |

## The line we do not cross

No genesis-era or Patoshi key has *ever* produced a verifying signature — only that would
upgrade Tier B from *attributable* to *proven*. Every public "I am Satoshi" claim
(including the BSV-side ones rejected in *COPA v Wright*, 2024) fails exactly this test.
The ≈1.1M BTC staying silent for 15+ years is itself the strongest ongoing statement: the
keys don't speak, and no impostor can make them.

Everything here is graded **[forensic], never [cryptographic]**.

## Repositories

- **[satoshi-onchain](https://github.com/satoshi-onchain/satoshi-onchain)** — a reproducible
  verifier + Patoshi classifier + coin-by-coin verdict tool. Faithfully reproduces Lerner's
  ExtraNonce/nonce-LSB analysis, refines the raw filter into a dormancy-validated estimate
  (~22.5k blocks, landing on Lerner two independent ways), and resolves any "Satoshi-era
  wallet moved N BTC" headline to `GENESIS / PATOSHI / AMBIGUOUS / NOT-PATOSHI`. Stdlib-only
  except plotting. MIT.

## The other half

**[original-bitcoin-laboratory](https://github.com/original-bitcoin-laboratory)** ·
[bitcoin-lab.org](https://bitcoin-lab.org) — an evidence-first, *executable* reconstruction of the
earliest Bitcoin: the November 2008 pre-release and the January 2009 v0.1.0 client, built from
hash-verified archives, with nothing disabled and no chain privileged.

Two halves of one question, answered with different evidence. That laboratory gets to the bottom of
**Bitcoin** by making the earliest code run and re-derive. This organization gets to the bottom of
**Satoshi** by measuring what the chain itself records. Neither leans on the other's conclusions.

<sub>Sources: S. D. Lerner, "The Well Deserved Fortune of Satoshi Nakamoto" (bitslog, 2013) for the ExtraNonce/nonce methodology; the chain itself for the genesis and block-170 facts. Reproducible-measurement discipline throughout.</sub>
