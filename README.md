# Benjamin Da Cunha

**Python Data Pipelines & Automation · Blockchain Intelligence · Statistical Validation**

Independent technical researcher, self-taught, building data and automation systems since December 2023. I take a badly defined question, build the tools to collect and rebuild the data, test whether my conclusions survive, and publish them so they can be checked.

My main investigation is on-chain: Solana memecoin launches, funding flows, coordinated wallets and the limits of predictive signals. The way of working is not tied to crypto.

---

## Featured: [Why Solana Memecoins Are Over](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over)

**€400 to start. $237,137.87 withdrawn.**

An investigation of pump.fun launches whose core offline pipeline reproduces byte for byte from a clone, from a pattern I traded in 2024 to the mechanism that replaced it in 2026.

* **2024.** I started with **€400**. Between **October and December 2024**, I withdrew **$237,137.87** trading memecoins on pump.fun. I traded a recurring pattern: fresh wallets funded through the same swap service hours before a launch, then buying in public. My withdrawals are reconstructed on chain from my own exchange deposit address.
* **2026.** On 42 launches of recurring buyer groups, rebuilt transaction by transaction, almost the entire bonding curve is bought in the block that creates the token: about 85 SOL for about 79% of the supply, with no public purchase before it. A selected sample, not a market-wide rate.
* **Can it be traded?** A live detector I built (its code is not public) alerted on 1,657 launches between 21 August and 29 September 2026. Nine studies, each with a written plan and a frozen input table, then one exploratory search over 415 features. Among the alerted launches, the buying wallets act as a group in about four out of five. One signal survived the held-out test and still lost money after costs: no tradable edge.
* **Negative results kept.** A buyer graph that put 63.8% of tokens in one component fell to 20.2% once nine infrastructure addresses were removed. The 2024 funding signature separated the tokens I traded from dead tokens only through a criterion that also fires on 88.9% of random wallet groups; without it, and against graduated tokens, it does not.

## What the repository shows

| Skill | Where to look |
|---|---|
| Python data pipelines | [`code/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/code): one script per measurement, standard library only; [`run_all.py --strict`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/code/run_all.py) reruns the 22 offline scripts and checks their tables and JSON byte for byte against the committed ones |
| API integration | [`rpc_client.py`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/code/rpc_client.py): a Solana RPC client with key rotation, a cooldown after HTTP 429 and bounded retries, where a failed call raises instead of returning an empty result; read-only calls to pump.fun, GeckoTerminal and Binance |
| Automation and CI | [`ci.yml`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/.github/workflows/ci.yml) on Python 3.12 and 3.13: byte-for-byte reproduction, a ledger that checks 43 of the README's figures against their artefacts, 76 unit tests, `mypy --strict`, `ruff`, a publication gate |
| Transaction analysis and fund tracing | [`02_cn_outflows.py`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/code/02_cn_outflows.py) (a swap service's hot-wallet outflows), [`exit_destination/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/exit_destination), [`funder_network/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/funder_network) |
| Detection and false positives | [`a1_null_model.py`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/code/a1_null_model.py): a funding detector tested against random wallet groups; one of its criteria fired on 88.9% of them and was retired |
| Statistical validation | [`post_detection_edge/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/post_detection_edge): signals locked before a held-out test, models written from scratch; cluster bootstraps, permutation and Fisher tests; a chained registry of every test run in the October 2026 search ([`alpha_patterns/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/alpha_patterns)) |
| Data-quality controls | [`PITFALLS.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/PITFALLS.md): an HTTP 403 that had become "no data", a network failure that looked like a result, a monitor that reported healthy while it was not |
| Attribution discipline | [`METHODOLOGY.md`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/blob/main/docs/METHODOLOGY.md): observed, inferred and attributed kept apart; exchange infrastructure recorded as not established rather than assigned to a person |

Not public: the live detector's code (a separate project).

## How I work

1. Write a falsifiable question and fix the population before computing any rate.
2. Rebuild the transactions and the chronology from the raw data.
3. Try to break the result: shared infrastructure, selection, missing data, lookahead, multiple testing, costs.
4. Publish what survives, and keep the corrections visible.

**Observed is not inferred, and inferred is not attributed.** Wallets can be linked on chain without proving who controls them.

I build with AI coding agents (Claude Code) every day: the commits they co-wrote carry a co-author line, and in October 2026 the pattern search and two of its follow-up studies were reviewed by AI audit agents before any outcome was computed ([`alpha_patterns/audit/`](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over/tree/main/alpha_patterns/audit)). The checks above let a reader rerun the offline pipeline and compare every tracked figure with the artefact behind it, instead of taking the code, mine or a model's, on trust.

## Background

Before this work I boxed professionally in France, the United States, Mexico and Colombia. Same habit on chain: observe, test, adapt, repeat.

## Contact

[contact@teamdacunha.com](mailto:contact@teamdacunha.com)
