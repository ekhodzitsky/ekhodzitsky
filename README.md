<div align="center">

# Evgeny Khodzitsky

**`Senior Backend · On-Device Speech AI · Agentic Systems`**

<img src="https://img.shields.io/github/followers/ekhodzitsky?style=flat-square&logo=github&label=Followers&color=0969DA" height="22">
<img src="https://img.shields.io/github/stars/ekhodzitsky?style=flat-square&logo=github&label=Stars&color=0969DA" height="22">
<img src="https://img.shields.io/github/repos/ekhodzitsky?style=flat-square&logo=github&label=Repos&color=0969DA" height="22">

</div>

---

### About

Senior backend engineer — **8+ years in production**.

- **Node.js / TypeScript** (NestJS, Moleculer) — REST APIs from scratch, API gateways, message brokers, payment & telephony integrations, legacy refactors at ~20k LOC scale.
- **Python** (FastAPI, Django) — email pipelines on APScheduler + SMTP, document generation (PDF/DOCX) at template-set scale.
- **Rust** — current focus: on-device speech AI and agentic developer tools.

Local-first by default: zero cloud APIs, zero vendor lock-in, models that ship inside the binary.

---

<div align="center">

<img src="https://img.shields.io/badge/Rust-000?logo=rust&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&style=flat-square" height="22">
<img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=flat-square" height="22">

</div>

---

### Open source

**Speech AI** — Rust + ONNX Runtime, fully offline. `cargo install …` or `pip install …`.

- [**`gigastt`**](https://github.com/ekhodzitsky/gigastt) — Russian STT (GigaAM v3) · **11.4% WER**, **~700 ms** for 16 s on M1, INT8 with 0% accuracy loss
- [**`polyvoice`**](https://github.com/ekhodzitsky/polyvoice) — Speaker diarization without Python · **DER ~14%** VoxConverse, **~23%** AMI · **10× realtime on CPU**, ~80% of pyannote accuracy
- [**`phonex`**](https://github.com/ekhodzitsky/phonex) — Generic on-device STT engine · **10+ languages**, ~70 ms / 5 s clip, single binary
- [**`nihostt`**](https://github.com/ekhodzitsky/nihostt) — Japanese STT (ReazonSpeech-k2-v2) · **CER ~1.1%** (clean) / **8%** (full 309-clip bench) · ~200 ms latency, INT8 ~155 MB
- [**`phostt`**](https://github.com/ekhodzitsky/phostt) — Vietnamese STT (Zipformer-vi RNN-T) · ~75 MB model · `crates.io` + `pypi`
- [**`localmt`**](https://github.com/ekhodzitsky/localmt) — Offline Android translation SDK · GGUF + llama.cpp via JNI, arm64-v8a target

**Agentic developer tools** — Kimi ecosystem

- [**`oh-my-kimi`**](https://github.com/ekhodzitsky/oh-my-kimi) — Wire-first orchestration for Kimi CLI · scheduler-backed teams, ownership conflict detection, verification gates, proof/failure artifacts
- [**`cargo-kimi`**](https://github.com/ekhodzitsky/cargo-kimi) — Cargo subcommand that scores Rust files **0–100** on contract quality (Hoare triples, panic safety, typestate, size, `Result` discipline) with LSP server · on `crates.io`
- [**`kimi-guidelines`**](https://github.com/ekhodzitsky/kimi-guidelines) — Composable configs, instructions, and skills for Kimi K2.6

---

<div align="center">

[![Telegram](https://img.shields.io/badge/-%40ekhodzitsky-2CA5E0?logo=telegram&logoColor=white&style=flat-square)](https://t.me/ekhodzitsky)
[![Habr](https://img.shields.io/badge/-Habr_Career-65A3BE?logo=habr&logoColor=white&style=flat-square)](https://career.habr.com/ekhodzitsky)

</div>
