<div align="center">

# Egor Khodzitsky

### AI/backend builder for local-first voice systems

<samp>REAL-TIME SPEECH / RUST BACKENDS / ON-DEVICE INFERENCE</samp>

I build the backend pieces for real-time translation and voice assistants:
speech recognition, speaker timelines, streaming APIs, and private inference runtimes.

[Telegram](https://t.me/ekhodzitsky) / [Email](mailto:e@khodzitsky.ru) / [Habr Career](https://career.habr.com/ekhodzitsky)

</div>

---

## Voice Lab

```text
audio in
   -> on-device STT
   -> speaker timeline
   -> translation / assistant core
   -> low-latency response loop
```

I care about systems that are fast enough to feel live, boring enough to run in production,
and private enough to work without shipping every word to a cloud API.

---

## Building Blocks

| Project | Signal | Role in the stack |
| --- | --- | --- |
| [gigastt](https://github.com/ekhodzitsky/gigastt) | Russian STT | Local GigaAM v3 speech server with WebSocket/REST, ONNX Runtime, CoreML/CUDA paths, and 10.4% WER benchmark notes. |
| [polyvoice](https://docs.rs/polyvoice/latest/polyvoice/) | Diarization | Rust library for online/offline speaker diarization: who spoke, when, and how to attach that to transcript words. |
| [phostt](https://docs.rs/crate/phostt/0.2.2) | Vietnamese STT | Zipformer-vi RNN-T server path for local Vietnamese speech recognition, built on the same real-time server ideas. |
| [nihostt](https://docs.rs/nihostt/latest/nihostt/) | Japanese STT | ReazonSpeech-k2-v2 based local Japanese STT runtime with VAD streaming and ONNX inference plumbing. |

These are not isolated demos. They are pieces of a broader voice stack:
language-specific STT, speaker awareness, streaming transport, and assistant-ready infrastructure.

---

## Operating Principles

- Local-first by default: no API keys as the happy path.
- Streaming before batch: partial results, backpressure, and protocol design matter.
- Rust where the edges are sharp: inference pools, typed errors, FFI, and long-running services.
- Production surface area: timeouts, limits, metrics, graceful shutdown, and sane defaults.

---

## Stack I Reach For

<p>
  <img src="https://img.shields.io/badge/Rust-111?logo=rust&logoColor=white&style=flat-square" alt="Rust">
  <img src="https://img.shields.io/badge/Tokio-111?logo=rust&logoColor=white&style=flat-square" alt="Tokio">
  <img src="https://img.shields.io/badge/Axum-111?logo=rust&logoColor=white&style=flat-square" alt="Axum">
  <img src="https://img.shields.io/badge/ONNX_Runtime-111?logo=onnx&logoColor=white&style=flat-square" alt="ONNX Runtime">
  <img src="https://img.shields.io/badge/TypeScript-111?logo=typescript&logoColor=white&style=flat-square" alt="TypeScript">
  <img src="https://img.shields.io/badge/PostgreSQL-111?logo=postgresql&logoColor=white&style=flat-square" alt="PostgreSQL">
</p>

---

<div align="center">

<samp>Building voice systems that can run close to the user.</samp>

</div>
