# Benjamin Da Cunha

**Vibe Coder · AI Builder · Automation · Rapid Prototyping · Python Systems**

I build working software with AI agents.

My strength is taking a vague problem, turning it into a concrete system, and getting it to work in the real world — fast. I use coding agents as my primary development environment, but I do not treat generated code as truth. I direct the build, connect the systems, test the weak points, debug failures and keep iterating until the result is useful.

I am a generalist by design. I work across automation, APIs, data pipelines, research tooling, device integrations and experimental products. I am comfortable entering a domain I do not know yet, learning what matters, and building around the actual problem rather than a preferred stack.

## What I do

- Build AI-assisted tools, automations and internal products
- Turn loosely defined ideas into working prototypes
- Orchestrate coding agents across larger technical tasks
- Connect APIs, data sources, desktop apps, mobile devices and hardware
- Build Python pipelines, detectors, monitors and research systems
- Add tests, CI, reproducibility and failure checks around AI-generated code
- Investigate technical problems deeply when the product requires it

**The goal is not to generate more code. The goal is to make the system work.**

---

## Featured investigation — [Why Solana Memecoins Are Over](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over)

**Started with €400. Withdrew $237,137.87 between October and December 2024.**

I found and traded a recurring on-chain pattern around pump.fun launches, then later rebuilt the research as a reproducible technical investigation.

The repository is not a victory lap. It shows the full process: what worked, what failed, what looked predictive but was not, and how I tested those conclusions.

Highlights:

- transaction-by-transaction reconstruction of Solana launches
- funding-flow and wallet-network analysis
- live detection infrastructure
- Python data pipelines and Solana RPC integration
- false-positive testing and null models
- held-out validation
- permutation, Fisher and bootstrap tests
- CI that reproduces committed outputs byte for byte
- 91 tests, `mypy --strict`, `ruff` and publication checks
- explicit separation between observed facts, inference and attribution

One result matters as much as the successful trade: when later testing failed to establish a profitable strategy under the measured conditions, I kept the negative result.

That is how I use AI-assisted development for serious work: speed up construction without lowering the standard of evidence.

---

## Featured project — [Spotify With YouTube](https://github.com/searadacunha/spotify-smarttube-bridge)

A Spotify-to-YouTube/SmartTube system for Android TV.

Choose a song on Spotify. The system identifies the corresponding YouTube publication and opens it automatically on SmartTube.

What looks simple on the surface required solving several real problems:

- distinguish the correct recording from remixes, live versions and alternate edits
- prefer official sources without blindly trusting titles
- compare audio when metadata is not enough
- cancel stale results when the Spotify track changes
- prevent the automation from fighting manual TV control
- deliver reliably over ADB
- validate behavior on real hardware

The repository includes CI on Python 3.12/3.13, a 93-test suite, explainable matching decisions, persistent deduplication and hardware-tested playback flows.

This is how I like to build: start with a real inconvenience, use AI agents to move fast, connect multiple systems, then harden everything that can fail.

---

## How I build

1. Define the result I actually want.
2. Break the problem into parts an AI agent can execute and verify.
3. Build the shortest path to a working version.
4. Connect it to real data, APIs, devices or users.
5. Test the failure modes, not just the happy path.
6. Iterate until it survives outside the demo.

I use Claude Code and other coding agents heavily. When agents contribute to public code, I keep the co-author attribution visible.

I care much more about whether a system works, can be checked and can survive edge cases than about who typed each line.

## Background

Before building software, I boxed professionally in France, the United States, Mexico and Colombia.

Different field, same operating style: learn fast, adapt under pressure, test against reality and keep moving.

## Contact

[contact@teamdacunha.com](mailto:contact@teamdacunha.com)
