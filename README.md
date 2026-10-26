# Benjamin Da Cunha

**I build things with AI.**

Self-taught vibe coder. I use Claude Code and Codex every day to turn ideas into working systems.

I don't care much about staying in one lane. If something is useful, weird, difficult to automate, or interesting enough, I'll probably try to build it.

## [Why Solana Memecoins Are Over](https://github.com/searadacunha/Why-Solana-Memecoins-Are-Over)

**€400 → $237,137.87 withdrawn in three months.**

In 2024 I found a recurring on-chain pattern around pump.fun launches and traded it.

Later I went back and tried to break my own thesis: rebuilt the transactions, traced the funding flows, wrote the tooling, tested false positives, ran held-out studies and published the negative results too.

The repo became much bigger than the original trade: Python pipelines, Solana RPC tooling, detection systems, statistical validation, CI, reproducible outputs and a lot of evidence for what *didn't* work.

It is probably the best representation of how I think.

## [Spotify With YouTube](https://github.com/searadacunha/Spotify-With-Youtube)

I wanted Spotify to automatically become the right music video on my TV, so I built it.

Spotify track in → edition-aware YouTube matching → SmartTube on Android TV.

The hard part was not opening a video. It was handling radio edits, remixes, live recordings, bad matches, stale searches and the fact that someone might be using the TV. The bridge combines metadata, audio comparison and a state-aware ADB handoff.

107 unit tests and real-TV playback runs. The README separates what worked on hardware from what still needs testing there.

## [YouTube Edit Ultra](https://github.com/searadacunha/YouTube-Edit-Ultra)

I wanted music-driven sports edits without cutting a goal, knockout or combination in half just to hit the beat.

It's a local Python/FFmpeg editing pipeline: source footage, action candidates or annotated sequences, music alignment, a rendered montage, thumbnail and YouTube metadata. Publishing is optional.

The tricky part is deciding *where an action really begins and ends*. The code protects annotated event windows and treats automatic motion detection as a starting point, not proof that it understood the play.

## [Stop-Bullshiting](https://github.com/searadacunha/Stop-Bullshiting)

Coding agents can read thousands of lines when the useful answer is buried in twenty. I wanted to keep the signal without losing the original output.

A local CLI for reducing noisy logs, finding exact lines and Python symbols, restoring full outputs and keeping project notes. It can connect to Claude Code and Codex through optional integrations and exposes tools over MCP.

It measures actual character reduction. It does **not** manufacture tokens or bypass account limits.

---

That is the kind of work I like.

Start with **“this should exist”**, use AI agents to move fast, stay on the hard decisions, and keep iterating until it works outside the demo.

Before software, I boxed professionally in France, the United States, Mexico and Colombia.

Different arena. Same instinct: **figure it out under pressure.**

[contact@teamdacunha.com](mailto:contact@teamdacunha.com)
