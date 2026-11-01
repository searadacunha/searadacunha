# Benjamin Da Cunha

**Vibe coder · Gambler... I mean trader · Independent on-chain researcher · Former professional boxer**

I trade crypto, investigate on-chain activity and build software through vibe coding. My projects range from Solana transaction analysis and statistical testing to media automation and tools for coding agents.

I use Python, Claude Code and Codex to turn ideas into working tools. I test what I build and share code, methods and evidence from my research.

## Selected work

### [Why Solana Memecoins Are Over](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over) · On-chain research

**From roughly €400 in starting capital to $237,137.87 withdrawn between October and December 2024.** The withdrawal figure is not itself a net-profit calculation.

A documented investigation of Solana / pump.fun activity: RPC extraction, wallet and funding-flow reconstruction, false-positive analysis, held-out testing and reproducible artifacts. The repository publishes failed hypotheses alongside positive findings instead of presenting backtests as guaranteed trading edges.

**Focus:** blockchain intelligence · transaction analysis · Python pipelines · statistical falsification

### [Spotify With YouTube](https://github.com/searadacunha/Spotify-With-Youtube) · TV automation

[![Tests](https://github.com/searadacunha/Spotify-With-Youtube/actions/workflows/tests.yml/badge.svg)](https://github.com/searadacunha/Spotify-With-Youtube/actions/workflows/tests.yml)

A local bridge that follows a Spotify track and selects a video for SmartTube on Android TV. It handles radio edits, remixes, source verification and optional audio comparison. Its ADB controller backs off if another app or user takes control of the TV.

**Focus:** Python · ADB · media metadata · audio matching · SQLite · hardware-aware automation

**Validation:** unit-tested workflows and documented real-TV playback trials; not every manual-override scenario has been hardware-tested.

### [YouTube Edit Ultra](https://github.com/searadacunha/YouTube-Edit-Ultra) · Sports editing

[![Quality checks](https://github.com/searadacunha/YouTube-Edit-Ultra/actions/workflows/ci.yml/badge.svg)](https://github.com/searadacunha/YouTube-Edit-Ultra/actions/workflows/ci.yml)

A Python/FFmpeg pipeline for assembling sports footage and music into local videos, thumbnails, storyboards and publishing metadata. The edit planner preserves supplied action windows instead of cutting a documented goal or combination to land on a beat.

**Focus:** Python · FFmpeg · event-driven editing · music alignment · optional YouTube upload

**Limit:** automatic motion detection proposes candidates; accurate event boundaries require annotations or reliable external spotting.

### [Stop-Bullshiting](https://github.com/searadacunha/Stop-Bullshiting) · Agent tooling

[![CI](https://github.com/searadacunha/Stop-Bullshiting/actions/workflows/ci.yml/badge.svg)](https://github.com/searadacunha/Stop-Bullshiting/actions/workflows/ci.yml)

A local CLI for reducing noisy command output, searching exact source lines and Python symbols, keeping project notes and recovering original logs. Optional Claude Code and Codex integrations, plus an MCP interface.

**Focus:** Python · CLI · MCP · AST · SQLite · local-first workflows

**Limit:** measures character reduction and reads available usage logs; it does **not** generate tokens or bypass provider quotas.

---

Before this work I boxed professionally in France, the United States, Mexico and Colombia. Same habit on chain: **observe, test, adapt, repeat.**

**Contact:** [contact@teamdacunha.com](mailto:contact@teamdacunha.com)
