<div align="center">

**`On-Device Speech AI · STT & Speaker Diarization · Senior Backend`**

<img src="https://img.shields.io/badge/Rust-000?logo=rust&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=flat-square" height="22">

</div>

---

### About

**Rust** — on-device speech AI that runs fully offline after a one-time model download, shipped as a single binary: speech-to-text ([`gigastt`](https://github.com/ekhodzitsky/gigastt)) and speaker diarization ([`polyvoice`](https://github.com/ekhodzitsky/polyvoice)) — the two projects I actively build — plus the zero-dependency WAVE codec underneath them ([`ryf`](https://github.com/ekhodzitsky/ryf)). Local-first by default: no cloud APIs at runtime, no vendor lock-in. On the side — agent & dev tooling experiments in Rust / Go (see the fold below).

**In private development** — Russian TTS on CosyVoice3, punctuation & casing restoration for ASR output, English-to-Russian video dubbing, semantic search over call recordings.

**Track record (Apr–Sep 2026, three speech repos)** — ~1,400 commits · ~160k lines of Rust · ~3,000 tests · 100+ tagged releases · weekly WER / DER benchmarks in CI · issues and feature requests from external users.

**Prior production backend** — Node.js / TypeScript (NestJS, Moleculer) and Python (FastAPI, Django): REST APIs and gateways from scratch, message brokers, payment & telephony integrations, large legacy refactors, and email / document (PDF/DOCX) pipelines.

---

### [`gigastt`](https://github.com/ekhodzitsky/gigastt) — on-device Russian speech recognition

**file RTF ~0.10 (≈10× real-time on M1 CPU) · 3.55% WER clean read (statistical tie vs Vosk) · phone calls 18.5% — beats Vosk and T-one · held-out Common Voice 2.63% — beats Vosk and faster-whisper · like-for-like 6-engine bench · one binary · no cloud at runtime**

```sh
cargo install gigastt && gigastt serve
# WebSocket: ws://127.0.0.1:9876/v1/ws
# REST API:  http://127.0.0.1:9876/v1/transcribe
```

GigaAM v3 + ONNX Runtime · INT8 ~225 MB · opt-in multilingual heads (ru/en/kk/ky/uz) · WebSocket streaming with Silero VAD end-of-utterance · speaker diarization via polyvoice · REST / SSE + async jobs · optional punctuation, casing & ITN · Android FFI + NNAPI · CPU / CoreML / CUDA · cargo / brew / npm / pip / Docker · 64 releases, 1.3k tests

### [`polyvoice`](https://github.com/ekhodzitsky/polyvoice) — speaker diarization for Rust

**Who spoke when, on CPU, without Python · ~15% DER VoxConverse-test (collar 0; pyannote 3.1 = 11.3%) · ~160× real-time on a laptop CPU · ~8.4 MB MIT INT8 models · 7.5k+ crates.io downloads**

```sh
cargo add polyvoice --features "pipeline-native,vbx"
```

Powerset segmentation + WeSpeaker embeddings + VBx (AHC / K-means / NME-SC alternatives) · overlap resegmentation · who-said-what via companion ASR crates · Rust / Python / C FFI / CLI / MCP · crates.io + PyPI

Powers the diarization feature in [`gigastt`](https://github.com/ekhodzitsky/gigastt), [`phonex`](https://github.com/ekhodzitsky/phonex), [`nihostt`](https://github.com/ekhodzitsky/nihostt) and [`phostt`](https://github.com/ekhodzitsky/phostt).

---

### More on-device speech

- [**`ryf`**](https://github.com/ekhodzitsky/ryf) — WAVE codec, zero default deps · PCM / IEEE float / G.711 / G.722 / GSM 06.10 / ADPCM · RIFF / RF64 / BW64 / Wave64 · ffmpeg as test oracle · WAV ingest for gigastt and polyvoice · `crates.io`
- [**`phonex`**](https://github.com/ekhodzitsky/phonex) — multilingual on-device STT engine · offline + streaming, single binary, HTTP / gRPC / FFI · `crates.io`
- [**`nihostt`**](https://github.com/ekhodzitsky/nihostt) — Japanese STT server (ReazonSpeech-k2-v2) · WebSocket / REST / SSE · `crates.io` + Homebrew + Docker
- [**`phostt`**](https://github.com/ekhodzitsky/phostt) — Vietnamese STT server (Zipformer-vi RNN-T) · streaming · `crates.io` + `pypi`
- [**`localmt`**](https://github.com/ekhodzitsky/localmt) — offline Android translation SDK · GGUF / llama.cpp via JNI · pre-release

<details>
<summary>Experiments — agent tooling, backend, archived</summary>

<br>

Side projects in varying states of maturity; not all actively maintained.

**Agent & dev tooling**

- [**`kimi-wire`**](https://github.com/ekhodzitsky/kimi-wire) — typed Rust client for the Kimi Code CLI Wire protocol · `crates.io` · Go twin: [`kimi-wire-go`](https://github.com/ekhodzitsky/kimi-wire-go)
- [**`mcp-guard`**](https://github.com/ekhodzitsky/mcp-guard) — guardian & stdio proxy for MCP servers (Go) · process pool, timeouts, tool permissions, rate limits, audit log
- [**`kimi-lite`**](https://github.com/ekhodzitsky/kimi-lite) — Go port of MoonshotAI's kimi-code coding CLI · single binary · MCP + ACP
- [**`gitr`**](https://github.com/ekhodzitsky/gitr) — async typed git wrapper for AI agents · JSON CLI + MCP server · library on `crates.io`
- [**`cargo-kimi`**](https://github.com/ekhodzitsky/cargo-kimi) — Cargo subcommand scoring Rust files 0–100 on contract quality · `crates.io`
- [**`coad`**](https://github.com/ekhodzitsky/coad) — written methodology for safe, reviewable, bounded coding-agent work
- [**`kimi-dotfiles`**](https://github.com/ekhodzitsky/kimi-dotfiles) — composable configs, instructions and skills for the Kimi CLI
- [**`jobsmith`**](https://github.com/ekhodzitsky/jobsmith) — AI job-application assistant for hh.ru · Rust TUI · Typst PDF CVs

**Backend**

- [**`go-ozon-marketplace`**](https://github.com/ekhodzitsky/go-ozon-marketplace) — portfolio pet project: e-commerce backend · 8 Go microservices + Rust API gateway · Saga · Outbox · CQRS · Kafka · ClickHouse · mTLS

**Archived**

- [**`omk`**](https://github.com/ekhodzitsky/omk) — Wire-first orchestration for Kimi CLI · archived June 2026 (post-mortem in the README)

</details>

---

<div align="center">

[![Telegram](https://img.shields.io/badge/-%40ekhodzitsky-2CA5E0?logo=telegram&logoColor=white&style=flat-square)](https://t.me/ekhodzitsky)
[![Email](https://img.shields.io/badge/-e%40khodzitsky.ru-EA4335?logo=gmail&logoColor=white&style=flat-square)](mailto:e@khodzitsky.ru)

</div>
