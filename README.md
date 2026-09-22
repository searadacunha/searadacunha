# Benjamin Da Cunha

**Blockchain Intelligence Analyst · On-Chain Forensics · Fraud Detection**

Former professional boxer turned self-taught blockchain analyst.

I investigate blockchain activity through **transaction reconstruction, funding-flow analysis, wallet behavior, temporal patterns, graph analysis, and adversarial validation**.

My work focuses on **Solana, blockchain forensics, transaction monitoring, fraud detection, funding flows, launch microstructure, and behavioral analysis**.

---

## Featured Investigation

### [Why Solana Memecoins Are Over](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over)

**A reproducible on-chain forensic investigation of pump.fun launch microstructure, wallet behavior, funding patterns, and a historical Solana trading signal.**

The research reconstructs blockchain activity at transaction level and tests whether apparently structured behavior remains significant after accounting for:

* shared infrastructure
* temporal co-occurrence
* selection and denominator effects
* missing data and measurement failures
* lookahead and multiple testing
* inappropriate control populations
* execution costs and market impact

The objective is not to find the strongest story in the data.

> **It is to find the strongest conclusion that survives attempts to break it.**

---

## From Trading Signal to Blockchain Intelligence

My entry into crypto was practical.

Through pattern recognition on Solana memecoins, I identified a recurring funding and accumulation structure and used it to execute trades.

One documented historical example took **$400 to $237,137.87 in withdrawals** during the period covered by the research.

When the market structure changed, I investigated the mechanism behind the historical edge rather than assuming the signal remained valid.

The investigation evolved into:

**observation → transaction reconstruction → fund-flow analysis → pattern detection → controls → adversarial testing → reproducible conclusion**

---

## Investigation Framework

The research follows a structured forensic workflow:

1. **Define a falsifiable question**
2. **Define the population and measurement rules**
3. **Reconstruct transactions and chronology**
4. **Trace funding and asset flows**
5. **Detect repeated structures**
6. **Test alternative explanations**
7. **Separate observation from attribution**
8. **Reproduce the result**

A recurring principle is:

**Observed ≠ Inferred ≠ Attributed**

Wallet similarity, shared infrastructure, or recurring execution patterns can establish relationships between on-chain entities without establishing the identity of a human operator.

---

## Key Findings

### Launch microstructure

Across **42 transaction-level reconstructed launches**:

* Median committed SOL: **85.21 SOL**
* Median supply acquired: **78.95%**
* Median launch market cap: **~$2,158**
* Median AMM-open market cap: **~$53,985**
* Intra-core timing gap: **0 slots in all 42**

### Buyer structures

The initial buyer graph contained **180 / 282 tokens (63.8%)** inside its largest connected component.

After removing nine high-ubiquity infrastructure addresses:

**57 / 282 (20.2%)** remained.

The investigation does not interpret these clusters as proof of a single operator.

### Historical funding pattern

Reproducible pre-launch funding structures involving fresh wallets and recurring funding amounts were identified across multiple tokens.

However, the control analysis **did not support the broader hypothesis** that the pattern was systematically more common among traded graduated tokens.

The case-level mechanism survived.

The broader prevalence claim did not.

### Trading-edge validation

The historical signal was tested under realistic detection and execution constraints.

Under the tested policies:

* **15 / 15** had negative mean returns
* **12 / 15** had negative median returns
* **0 / 15** had confidence intervals above zero
* +1h median multiple: **0.48×**
* +24h median multiple: **0.20×**

The tested post-detection policies did not demonstrate positive measured expectancy on the declared population.

---

## Methodological Discipline

The investigation is built around several principles:

* A detector must survive a **null model**
* Controls must resemble the **target population**
* **Missing data is not zero**
* Historical knowledge cannot enter a supposedly live strategy
* **Identity requires evidence**
* Corrections remain visible

When a measurement is superseded by a better reconstruction, the correction is documented rather than silently replaced.

---

## Reproducibility

The repository is backed by:

* public on-chain data
* committed datasets and derived artefacts
* deterministic Python scripts
* explicit measurement definitions
* validation scripts
* reproducible tables and JSON outputs
* documented methodological corrections

The research is structured so the reader can move from:

**claim → measurement → code → data → validation**

rather than taking the narrative on trust.

---

## Repository Structure

| File                    | Purpose                                  |
| ----------------------- | ---------------------------------------- |
| `docs/INVESTIGATION.md` | Forensic workflow                        |
| `docs/METHODOLOGY.md`   | Definitions and measurement methodology  |
| `docs/RESULTATS.md`     | Main results                             |
| `docs/PITFALLS.md`      | Attempts to invalidate findings          |
| `docs/PATTERN.md`       | Historical funding-pattern investigation |
| `docs/SPLIT_PHASE1.md`  | Controlled historical investigation      |
| `docs/EXPLOITATION.md`  | Historical trading and signal record     |
| `code/README.md`        | Analysis pipeline and reproducibility    |

---

## Background

Before working on blockchain research, I competed as a professional boxer in **France, the United States, Mexico and Colombia**.

That background still influences how I approach investigations:

**observe → test → adapt → repeat**

I apply the same discipline to on-chain research: work from the evidence, challenge the first explanation, and keep the conclusion proportional to what the data can establish.

---

## Contact

For research, collaboration and professional inquiries:

**[contact@teamdacunha.com](mailto:contact@teamdacunha.com)**
