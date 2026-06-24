<div align="center">

**`On-Device Speech AI · Agentic Systems · Senior Backend`**

<img src="https://img.shields.io/badge/Rust-000?logo=rust&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=flat-square" height="22">

</div>

---

### About

**Rust / Go** — on-device speech AI and agentic developer tools: STT and speaker-diarization engines that run fully offline and ship inside a single binary, plus typed clients and guardrails for AI coding agents. Local-first by default: zero cloud APIs, zero vendor lock-in, models that ship inside the binary.

**Prior production backend** — Node.js / TypeScript (NestJS, Moleculer) and Python (FastAPI, Django): REST APIs and gateways from scratch, message brokers, payment & telephony integrations, large legacy refactors, and email / document (PDF/DOCX) pipelines.

---

### Flagship — [`gigastt`](https://github.com/ekhodzitsky/gigastt)

**On-device Russian speech recognition — live WebSocket streaming, RTF ~0.1 (≈10× real-time on M1). 3.55% WER (golos_crowd_1k, in-domain). One binary. No cloud.**

```sh
cargo install gigastt && gigastt serve
# WebSocket: ws://127.0.0.1:9876/v1/ws
# REST API:  http://127.0.0.1:9876/v1/transcribe
```

GigaAM v3 + ONNX Runtime · INT8 with 0% WER loss · WebSocket streaming + REST · Homebrew tap · CoreML / CUDA / CPU

---

### Open source

**Speech AI** — Rust + ONNX Runtime, fully offline

- [**`polyvoice`**](https://github.com/ekhodzitsky/polyvoice) — speaker diarization without Python · **~18.5% DER** VoxConverse-test (collar 0; pyannote 3.1 = 11.3%) · `crates.io` + `pypi`
- [**`phonex`**](https://github.com/ekhodzitsky/phonex) — generic on-device STT engine · **12 languages**, single binary · `crates.io`

**Agentic developer tools**

- [**`kimi-wire`**](https://github.com/ekhodzitsky/kimi-wire) — typed Rust client for the Kimi Code CLI **Wire protocol** · typed events, pluggable transports, secret redaction · Go twin: [`kimi-wire-go`](https://github.com/ekhodzitsky/kimi-wire-go)
- [**`mcp-guard`**](https://github.com/ekhodzitsky/mcp-guard) — production guardian & **proxy for MCP servers** · process pool, timeouts, audit logging, rate limiting, tool permissions
- [**`kimi-lite`**](https://github.com/ekhodzitsky/kimi-lite) — native AI coding CLI in **Go** · single binary, zero runtime deps

**Backend**

- [**`go-ozon-marketplace`**](https://github.com/ekhodzitsky/go-ozon-marketplace) — Go microservices e-commerce backend · 8 services · Saga · Outbox · CQRS · Kafka · ClickHouse · mTLS

<details>
<summary>More — STT engines, on-device translation, agent tooling</summary>

- [**`nihostt`**](https://github.com/ekhodzitsky/nihostt) — Japanese STT (ReazonSpeech-k2-v2) · **CER ~1.1%** (clean) · INT8 ~155 MB · `crates.io`
- [**`phostt`**](https://github.com/ekhodzitsky/phostt) — Vietnamese STT (Zipformer-vi RNN-T) · ~75 MB model · `crates.io` + `pypi`
- [**`localmt`**](https://github.com/ekhodzitsky/localmt) — offline Android translation SDK in Rust · GGUF/Hy-MT packs, llama.cpp via JNI, arm64-v8a
- [**`cargo-kimi`**](https://github.com/ekhodzitsky/cargo-kimi) — Cargo subcommand scoring Rust files **0–100** on contract quality (Hoare triples, panic safety, typestate, `Result` discipline) · `crates.io`
- [**`coad`**](https://github.com/ekhodzitsky/coad) — Contract-Orchestrated Agent Development · methodology for safe, reviewable, bounded agent work
- [**`kimi-dotfiles`**](https://github.com/ekhodzitsky/kimi-dotfiles) — composable configs, instructions, and skills for Kimi K2.6
- [**`gitr`**](https://github.com/ekhodzitsky/gitr) — async **typed git CLI** wrapper for agents and automation · JSON output, MCP server · `crates.io`
- [**`omk`**](https://github.com/ekhodzitsky/omk) — Wire-first orchestration for Kimi CLI · archived June 2026 (post-mortem in the README)

</details>

---

<div align="center">

[![Telegram](https://img.shields.io/badge/-%40ekhodzitsky-2CA5E0?logo=telegram&logoColor=white&style=flat-square)](https://t.me/ekhodzitsky)
[![Email](https://img.shields.io/badge/-e%40khodzitsky.ru-EA4335?logo=gmail&logoColor=white&style=flat-square)](mailto:e@khodzitsky.ru)

</div>
