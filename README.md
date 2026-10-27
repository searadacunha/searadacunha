# Benjamin Da Cunha

**I build things with AI.**

Independent builder and on-chain researcher. Self-taught, using Claude Code and Codex to turn ideas into working tools.

My projects start with a concrete problem: connect Spotify to the right music video, preserve a complete action in a sports edit, or make an agent's terminal output useful without losing the original.

[Contact](mailto:contact@teamdacunha.com) · [All repositories](https://github.com/searadacunha?tab=repositories)

## [Why Solana Memecoins Are Over](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over)

**€400 → $237,137.87 withdrawn in three months.**

In 2024 I found a recurring on-chain pattern around pump.fun launches and traded it.

Later I went back and tried to break my own thesis: rebuilt the transactions, traced the funding flows, wrote the tooling, tested false positives, ran held-out studies and published the negative results too.

The repo became much bigger than the original trade: Python pipelines, Solana RPC tooling, detection systems, statistical validation, CI, reproducible outputs and a lot of evidence for what *didn't* work.

It is probably the best representation of how I think.

## Tools

| Project | What it does | Built with |
| --- | --- | --- |
| [**YouTube Edit Ultra**](https://github.com/searadacunha/YouTube-Edit-Ultra) | Builds music-driven sports edits with protected action windows, thumbnails and upload metadata. | Python · FFmpeg |
| [**Spotify With YouTube**](https://github.com/searadacunha/Spotify-With-Youtube) | Matches Spotify tracks to YouTube videos and hands playback to SmartTube while respecting manual TV use. | Python · ADB · SQLite |
| [**Stop-Bullshiting**](https://github.com/searadacunha/Stop-Bullshiting) | Reduces noisy terminal output, retrieves exact source lines and keeps full outputs available locally. | Python · CLI · MCP |

### YouTube Edit Ultra

Sports edits should keep the goal, knockout or combination intact. This local pipeline combines source footage, action candidates or annotated sequences, music alignment and FFmpeg rendering. Publishing is optional.

The difficult part is deciding where an action begins and ends. Annotated event windows are protected; automatic motion detection produces candidates that still need review.

[Quick start and examples →](https://github.com/searadacunha/YouTube-Edit-Ultra#readme)

### Spotify With YouTube

Choose the track in Spotify; watch its video in SmartTube. The bridge considers artists, radio edits, remixes, live recordings and audio similarity before handing playback to Android TV.

It distinguishes verified matches from popularity-based fallbacks, discards stale searches and tracks whether it still owns the TV session. The documentation separates recorded hardware observations from automated tests and checks still to perform.

[Setup, matching logic and verification →](https://github.com/searadacunha/Spotify-With-Youtube#readme)

### Stop-Bullshiting

Coding agents can read thousands of lines when the useful answer is buried in twenty. This CLI reduces noisy logs, finds exact lines and Python symbols, restores full outputs and keeps project notes. Optional integrations connect it to Claude Code, Codex and MCP clients.

It measures character reduction. It does **not** manufacture tokens, expand subscriptions or bypass account limits.

[Installation, commands and integrations →](https://github.com/searadacunha/Stop-Bullshiting#readme)

## How I work

- Start with a problem I actually have.
- Use AI agents to move quickly, then inspect the code and test the behavior.
- Keep measurements, limitations and negative results visible.
- Make the next person's first run easier: clear setup, concrete examples and useful diagnostics.

---

Before software, I boxed professionally in France, the United States, Mexico and Colombia.

Different arena. Same instinct: **figure it out under pressure.**

[contact@teamdacunha.com](mailto:contact@teamdacunha.com)
