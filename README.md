# Benjamin Da Cunha

**Vibe Coder · AI Automation · Rapid Prototyping · Python Systems**

I am a self-taught **vibe coder and AI builder**. I use coding agents as my primary development environment to turn rough ideas into working software quickly: automations, data pipelines, API integrations, research tools, device-to-device workflows and experimental products.

I am not specialized in one vertical. I like problems where the starting point is unclear and the useful output is something concrete that works. I can move from an idea to a prototype, test it against reality, break what is unreliable, and iterate fast.

Blockchain analysis is one of the areas where I have applied that approach successfully — including an on-chain pattern I traded in 2024 — but it is not the limit of what I build.

---

## What I build

- AI-assisted software and internal tools
- workflow automation and agent-driven systems
- Python data pipelines and API integrations
- rapid prototypes from loosely defined requirements
- research tooling, detectors and monitoring systems
- integrations across desktop, mobile, Android TV and connected devices
- validation layers around AI-generated code: tests, CI, reproducibility and failure checks

I work with AI coding agents every day, especially Claude Code, and treat them as force multipliers rather than sources of truth. The speed comes from the agents; reliability comes from verification.

## Featured: [Spotify With YouTube](https://github.com/searadacunha/spotify-smarttube-bridge)

A Spotify-to-YouTube/SmartTube bridge built for Android TV. It detects the current Spotify track, searches YouTube, identifies the correct recording and edition, rejects the wrong remix/live/edit when necessary, and opens the best matching video automatically on SmartTube.

The project goes beyond a simple title search: it uses artist identity, edition parsing, duration checks, official-source preference and, when metadata is ambiguous, audio comparison. It also checks that Spotify has not changed tracks before sending, and includes a user-priority guard so the automation does not fight manual TV control.

The repository documents real hardware tests, explainable matching decisions, stale-result cancellation, persistent deduplication, ADB delivery, CI on Python 3.12/3.13 and a 93-test suite.

This is a representative vibe-coding project for me: start with a practical problem, use agents to build fast, connect several systems, test on real hardware, then harden the weak points.

## Featured: [Why Solana Memecoins Are Over](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over)

**€400 to start. $237,137.87 withdrawn.**

An investigation of pump.fun launches whose core offline pipeline reproduces byte for byte from a clone, from a pattern I traded in 2024 to a different launch mechanism measured in 2026.

* **2024.** I started with **€400**. Between **October and December 2024**, I withdrew **$237,137.87** trading memecoins on pump.fun. I traded a recurring pattern: fresh wallets funded through the same swap service hours before a launch, then buying in public. My withdrawals are reconstructed on chain from my own exchange deposit address. This measures deposits, not a complete trading PnL.
* **2026.** On 42 launches of recurring buyer groups, rebuilt transaction by transaction, almost the entire bonding curve is bought in the block that creates the token: about 85 SOL for about 79% of the supply. A selected sample, not a market-wide rate.
* **Can it be traded?** A live detector I built (its code is not public) alerted on 1,657 launches between 21 August and 29 September 2026. Nine studies, each with a written plan and a frozen input table, then one exploratory search over 415 features. Among the alerted launches, the buying wallets act as a group in about four out of five. One signal survived the held-out test and still lost money after costs: no profitable strategy established under the tested conditions.
* **Negative results kept.** A buyer graph that put 63.8% of tokens in one component fell to 20.2% once nine infrastructure addresses were removed. The 2024 funding signature separated the tokens I traded from dead tokens only through a criterion that also fires on 88.9% of random wallet groups; without it, and against graduated tokens, it does not.

## What the repository shows

| Skill | Where to look |
|---|---|
| Python data pipelines | [`code/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/code): one script per measurement, standard library only; [`run_all.py --strict`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/code/run_all.py) reruns the 22 offline scripts and checks their tables and JSON byte for byte against the committed ones |
| API integration | [`rpc_client.py`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/code/rpc_client.py): a Solana RPC client with key rotation, a cooldown after HTTP 429 and bounded retries, where a failed call raises instead of returning an empty result; read-only calls to pump.fun, GeckoTerminal and Binance |
| Automation and CI | [`ci.yml`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/.github/workflows/ci.yml) on Python 3.12 and 3.13: byte-for-byte reproduction, a ledger that checks 43 of the README's figures against their artefacts, 91 tests, `mypy --strict`, `ruff`, a publication gate |
| Transaction analysis and fund tracing | [`02_cn_outflows.py`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/code/02_cn_outflows.py) (a swap service's hot-wallet outflows), [`exit_destination/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/exit_destination), [`funder_network/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/funder_network) |
| Detection and false positives | [`a1_null_model.py`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/code/a1_null_model.py): a funding detector tested against random wallet groups; one of its criteria fired on 88.9% of them and was retired |
| Statistical validation | [`post_detection_edge/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/post_detection_edge): signals locked before a held-out test, models written from scratch; cluster bootstraps, permutation and Fisher tests; a chained registry of every test run in the October 2026 search ([`alpha_patterns/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/alpha_patterns)) |
| Data-quality controls | [`PITFALLS.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/PITFALLS.md): an HTTP 403 that had become "no data", a network failure that looked like a result, a monitor that reported healthy while it was not |
| Attribution discipline | [`METHODOLOGY.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/METHODOLOGY.md): observed, inferred and attributed kept apart; exchange infrastructure recorded as not established rather than assigned to a person |

Not public: the live detector's code (a separate project).

## How I work

1. Start from the outcome, not from a preferred technology.
2. Use AI agents to get to a working implementation quickly.
3. Connect the real systems: APIs, devices, data sources, automation and interfaces.
4. Test the parts that can silently fail.
5. Keep iterating until the result is useful outside the demo.

For analytical work, I use the same discipline more formally: define the population, rebuild the chronology, test alternative explanations, measure false positives and keep negative results visible.

**Observed is not inferred, and inferred is not attributed.**

The commits co-written by coding agents carry a co-author line. In the Solana research, AI audit agents also reviewed parts of the experimental process before outcomes were computed ([`alpha_patterns/audit/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/alpha_patterns/audit)).


## Background

Before this work I boxed professionally in France, the United States, Mexico and Colombia. Same habit on chain: observe, test, adapt, repeat.

## Contact

[contact@teamdacunha.com](mailto:contact@teamdacunha.com)
