<div align="center">

**`Senior Backend · On-Device Speech AI · Agentic Systems`**

</div>

---

### About

- **Node.js / TypeScript** (NestJS, Moleculer) — REST APIs from scratch, API gateways, message brokers, payment & telephony integrations, legacy refactors at ~20k LOC scale.
- **Python** (FastAPI, Django) — email pipelines on APScheduler + SMTP, document generation (PDF/DOCX) at template-set scale.
- **Rust / Go** — current focus: on-device speech AI and agentic developer tools.

Local-first by default: zero cloud APIs, zero vendor lock-in, models that ship inside the binary.

**Currently shipping:** [`mcp-guard`](https://github.com/ekhodzitsky/mcp-guard) · [`kimi-lite`](https://github.com/ekhodzitsky/kimi-lite)

---

<div align="center">

<img src="https://img.shields.io/badge/Rust-000?logo=rust&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=flat-square" height="22">

</div>

---

### 🚀 Flagship — [`gigastt`](https://github.com/ekhodzitsky/gigastt)

**Russian speech recognition on M1 — 16 s of audio in ~700 ms (encoder). 8.6% WER (golos_crowd_1k). One binary. No cloud.**

```sh
cargo install gigastt && gigastt serve
# WebSocket: ws://127.0.0.1:9876/v1/ws
# REST API:  http://127.0.0.1:9876/v1/transcribe
```

GigaAM v3 + ONNX Runtime · INT8 with 0% WER loss · WebSocket streaming + REST · Homebrew tap · CoreML / CUDA / CPU

---

### Open source

**Speech AI** — Rust + ONNX Runtime, fully offline

- [**`polyvoice`**](https://github.com/ekhodzitsky/polyvoice) — Speaker diarization without Python · **DER ~14%** VoxConverse (232 files, 0.25 s collar) · **~10× realtime on CPU**, ~80% of pyannote accuracy · `crates.io` + `pypi`
- [**`phonex`**](https://github.com/ekhodzitsky/phonex) — Generic on-device STT engine · **10 languages**, ~70 ms / 5 s clip, single binary · `crates.io` + `pypi`
- [**`nihostt`**](https://github.com/ekhodzitsky/nihostt) — Japanese STT (ReazonSpeech-k2-v2) · **CER ~1.1%** (clean) / **~8%** (full 309-clip bench) · ~200 ms latency, INT8 ~155 MB · `crates.io`
- [**`phostt`**](https://github.com/ekhodzitsky/phostt) — Vietnamese STT (Zipformer-vi RNN-T) · ~75 MB model · `crates.io` + `pypi`

**On-device translation** — Rust + llama.cpp, fully offline

- [**`localmt`**](https://github.com/ekhodzitsky/localmt) — Offline Android translation SDK in Rust · **GGUF/Hy-MT** packs, llama.cpp via JNI, arm64-v8a

**Agentic developer tools**

*Kimi ecosystem*

- [**`kimi-wire`**](https://github.com/ekhodzitsky/kimi-wire) — Typed Rust client for the Kimi Code CLI **Wire protocol** · typed events, pluggable transports, secret redaction · Go twin: [`kimi-wire-go`](https://github.com/ekhodzitsky/kimi-wire-go)
- [**`kimi-lite`**](https://github.com/ekhodzitsky/kimi-lite) — Native AI coding CLI in **Go** · single binary, zero runtime deps
- [**`cargo-kimi`**](https://github.com/ekhodzitsky/cargo-kimi) — Cargo subcommand that scores Rust files **0–100** on contract quality (Hoare triples, panic safety, typestate, size, `Result` discipline) with LSP server · `crates.io`
- [**`coad`**](https://github.com/ekhodzitsky/coad) — **Contract-Orchestrated Agent Development** · methodology for safe, reviewable, bounded agent work
- [**`kimi-dotfiles`**](https://github.com/ekhodzitsky/kimi-dotfiles) — Composable configs, instructions, and skills for Kimi K2.6
- [**`omk`**](https://github.com/ekhodzitsky/omk) — Wire-first orchestration for Kimi CLI · **archived June 2026** after upstream replaced the Wire protocol with ACP — post-mortem in the README

*General agent tooling*

- [**`mcp-guard`**](https://github.com/ekhodzitsky/mcp-guard) — Production guardian & **proxy for MCP servers** · process pool, hard timeouts, audit logging, rate limiting, tool permissions
- [**`gitr`**](https://github.com/ekhodzitsky/gitr) — Async **typed git CLI** wrapper for agents and automation · JSON output, MCP server · `crates.io`

---

<div align="center">

[![Telegram](https://img.shields.io/badge/-%40ekhodzitsky-2CA5E0?logo=telegram&logoColor=white&style=flat-square)](https://t.me/ekhodzitsky)
[![Email](https://img.shields.io/badge/-e%40khodzitsky.ru-EA4335?logo=gmail&logoColor=white&style=flat-square)](mailto:e@khodzitsky.ru)

</div>
