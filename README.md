# Benjamin Da Cunha

**Blockchain Intelligence Analyst · On-Chain Forensics · Fraud Detection**

Former professional boxer turned self-taught blockchain analyst.

I investigate blockchain activity through transaction reconstruction, funding-flow analysis, wallet behavior, temporal patterns, graph analysis, and adversarial validation.

My work focuses on **Solana, blockchain forensics, transaction monitoring, fraud detection, funding flows, launch microstructure, and behavioral analysis**.

---

## Featured Investigation

### [Why Solana Memecoins Are Over](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over)

A reproducible on-chain forensic investigation of **pump.fun launch microstructure, wallet behavior, funding patterns, and the evolution of a historical Solana trading signal**.

The project reconstructs blockchain activity at transaction level and tests whether apparently structured behavior remains significant after accounting for:

* shared infrastructure;
* temporal co-occurrence;
* selection effects;
* denominator effects;
* missing data;
* measurement failures;
* lookahead;
* multiple testing;
* inappropriate control populations;
* execution costs and market impact.

The repository does not only present the observations that survived.

It also documents **failed hypotheses, methodological failures, corrected measurements, alternative explanations, and conclusions that did not survive testing.**

> **The objective is not to find the strongest story in the data. It is to find the strongest conclusion that survives attempts to break it.**

---

## From Market Observation to Blockchain Intelligence

My entry into crypto was practical.

Through observation and pattern recognition on Solana memecoins, I identified a recurring funding and accumulation structure and used it to execute a series of trades.

One documented historical example took **$400 to $237,137.87** in withdrawals during the period covered by the research.

The interesting part of the story is not simply the result.

When the market structure changed, I investigated the mechanism behind the historical edge rather than assuming that the same signal remained valid.

That investigation evolved into a broader study of:

```text
on-chain observation
        ↓
transaction reconstruction
        ↓
fund-flow analysis
        ↓
pattern detection
        ↓
alternative explanations
        ↓
null models / controls
        ↓
adversarial testing
        ↓
reproducible conclusion
```

The result is a research process designed to distinguish **what happened, how it happened, and what can actually be attributed to it.**

---

## Investigation Framework

The repository uses a consistent forensic workflow.

### 01 — Define the question

Start with a specific, falsifiable question.

Not:

> "Are these wallets coordinated?"

But:

> "Do these wallets exhibit a funding structure that is unusual relative to an appropriate control population?"

---

### 02 — Define the population

Every measurement is tied to an explicit:

* time window;
* token population;
* inclusion criteria;
* exclusion criteria;
* measurement availability;
* capture method;
* missing-data policy.

This prevents the outcome from silently defining the sample.

---

### 03 — Reconstruct the evidence

Transactions are reconstructed before interpretation.

Depending on the investigation, this includes:

* wallet creation and activity;
* SOL transfers;
* token purchases;
* token sales;
* funding transactions;
* transaction chronology;
* launch events;
* downstream transfers;
* recurring wallet relationships.

---

### 04 — Trace the flow

Funding investigations follow assets through the chain:

```text
source
  ↓
gateway / distributor
  ↓
fresh wallet
  ↓
token purchase
  ↓
secondary wallet / liquidation
```

The chronology matters.

A funding event occurring after a token purchase cannot be used as evidence that the funding financed that purchase.

---

### 05 — Detect repeated structures

Patterns are identified through combinations of observable properties such as:

* common funding transactions;
* similar funding amounts;
* temporal proximity;
* wallet freshness;
* pre-launch funding;
* repeated execution structures;
* cross-token recurrence;
* downstream wallet behavior.

A single shared attribute is not automatically treated as evidence of common control.

---

### 06 — Test alternative explanations

Every significant observation is challenged.

Examples include:

* shared infrastructure;
* common services;
* temporal concentration;
* selection bias;
* denominator effects;
* missingness;
* transport failures;
* lookahead;
* multiple testing;
* inappropriate controls.

This is documented explicitly in [`docs/PITFALLS.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/PITFALLS.md).

---

### 07 — Separate observation from attribution

The investigation distinguishes between:

**Observed**

> Four wallets received the same amount in the same funding transaction.

**Supported inference**

> The structure is consistent with a repeatable funding mechanism.

**Not established**

> The wallets belong to one specific person or organization.

The same principle applies to gateways, infrastructure, software patterns, and graph clusters.

---

### 08 — Reproduce

A conclusion is not considered complete until its underlying measurement can be reproduced from the committed data and analysis code.

---

## What the Main Investigation Found

The current study produced several findings that survived the documented validation process.

### Launch microstructure

Across **42 transaction-level reconstructed launches**:

* median committed SOL: **85.21 SOL**;
* median supply acquired: **78.95%**;
* curve purchases before the creation block: **0 / 42**;
* intra-core timing gap: **0 slots in all 42**;
* median transfer delay: **17.5 seconds**;
* median launch market cap: approximately **$2,158**;
* median AMM-open market cap: approximately **$53,985**.

The measured structure shows that substantial acquisition and repricing occurred inside the launch mechanism before external market participation became observable.

---

### Repricing

The reconstructed price ladder showed a substantial transition between creation and external market visibility.

Median values:

```text
Launch                  ~$2,158
Creation block         ~$8,321
After final ticket    ~$26,093
AMM first external    ~$53,985
```

The independent capture set showed a comparable launch-to-AMM-open multiple of approximately **25×**.

The important distinction is between **observable repricing** and any claim about future price direction.

---

### Buyer structures

The initial buyer graph contained:

**180 / 282 tokens — 63.8%**

inside its largest connected component.

After removing nine high-ubiquity infrastructure addresses:

**57 / 282 — 20.2%**

remained.

Several persistent buyer structures remained after this adjustment, including clusters with very high wallet reuse.

The investigation does **not** interpret those clusters as proof of a single human operator.

Infrastructure, software reuse, and shared execution mechanisms remain alternative explanations.

---

### Historical funding pattern

The historical investigation identified reproducible pre-launch funding structures involving fresh wallets and recurring funding amounts.

In the measured historical population, the mechanism was observed across multiple tokens.

However, the appropriate control analysis did not support the broader original hypothesis that the pattern was systematically more common among traded graduated tokens.

The case-level mechanism survived.

The broader prevalence claim did not.

That distinction is central to the research.

---

### Trading-edge validation

The later market analysis tested whether the historical signal still produced positive results after realistic detection and execution constraints.

Under the tested policies:

* **15 / 15** had negative mean returns;
* **12 / 15** had negative median returns;
* **0 / 15** had confidence intervals above zero;
* +1h median multiple: **0.48×**;
* +24h median multiple: **0.20×**;
* whole-population +24h multiple: approximately **0.03×**.

These results do not establish that every possible strategy fails.

They establish that the tested post-detection policies did not demonstrate positive measured expectancy on the declared population.

---

## Methodological Discipline

Several principles govern the research.

### A detector must survive a null model

An apparently strong relationship can occur naturally when the underlying population is highly connected.

### A control must resemble the target

Comparing successful targets against failed launches can manufacture an apparent association.

### Missing data is not zero

An RPC failure, HTTP error, pagination limit, or provider cap is recorded as a measurement problem rather than converted into a negative observation.

### Historical knowledge cannot enter a live strategy

Future peaks, troughs, or outcomes cannot be used to construct an entry that would not have been available at the time.

### Identity requires evidence

Wallet similarity, shared infrastructure, and recurring execution patterns can establish relationships between on-chain entities without establishing the identity of the human operator.

### Corrections remain visible

When a published measurement is superseded by a better reconstruction, the correction is documented rather than silently replaced.

---

## Research Structure

The repository is organized around several complementary layers.

| File                                                                                                                     | Purpose                                              |
| ------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------- |
| [`docs/INVESTIGATION.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/INVESTIGATION.md) | Investigation framework and forensic workflow        |
| [`docs/METHODOLOGY.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/METHODOLOGY.md)     | Definitions, populations and measurement methodology |
| [`docs/RESULTATS.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/RESULTATS.md)         | Main measured results                                |
| [`docs/PITFALLS.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/PITFALLS.md)           | Attempts to invalidate the findings                  |
| [`docs/PATTERN.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/PATTERN.md)             | Historical funding-pattern investigation             |
| [`docs/SPLIT_PHASE1.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/SPLIT_PHASE1.md)   | Controlled historical investigation                  |
| [`docs/EXPLOITATION.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/EXPLOITATION.md)   | Historical trading and signal-discovery record       |
| [`code/README.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/code/README.md)               | Analysis pipeline and reproducibility                |

---

## Reproducibility

The analysis is backed by:

* public on-chain data;
* committed datasets and derived artefacts;
* deterministic Python scripts;
* explicit measurement definitions;
* documented corrections;
* validation scripts;
* reproducible tables and JSON outputs.

The core analysis can be reproduced without credentials once the required data is present locally.

The repository is deliberately structured so that the reader can move from:

**claim → measurement → code → data → validation**

rather than having to take the narrative on trust.

---

## Background

Before working full-time on blockchain research, I competed as a professional boxer in **France, the United States, Mexico and Colombia**.

That background still influences how I approach investigations:

**observe → test → adapt → repeat.**

I bring the same discipline to on-chain research: work from the evidence, challenge the first explanation, and keep the conclusion proportional to what the data can actually establish.

---

## Contact

For research, collaboration and professional inquiries:

**[contact@teamdacunha.com](mailto:contact@teamdacunha.com)**

[Instagram — @benjamindacunha](https://instagram.com/benjamindacunha)
