# Project Overview: Handy

Handy is a free, open source, and extensible speech-to-text application that works completely offline. It is a cross-platform desktop application built with Tauri (Rust + React/TypeScript) that provides simple, privacy-focused speech transcription.

## Key Features
- **Offline Transcription**: Uses Whisper and Parakeet models locally.
- **Privacy-Focused**: Voice stays on the computer; no cloud processing.
- **Cross-Platform**: Windows, macOS, and Linux.
- **Workflow**: Press global shortcut -> Speak -> Release -> Text pasted into any text field.
- **VAD**: Uses Silero VAD for silence filtering.

## Tech Stack
- **Framework**: Tauri 2.x
- **Frontend**: React + TypeScript, Tailwind CSS, Vite, Zustand (state).
- **Backend**: Rust
- **Package Manager**: Bun
- **ML Inference**: `whisper-rs`, `transcription-rs`, `vad-rs` (Silero).
- **Audio I/O**: `cpal`
- **System Events**: `rdev` (shortcuts/typing).

## Structure
- `src/`: React frontend (Settings UI, overlay).
- `src-tauri/`: Rust backend.
  - `src/managers/`: Core logic (Audio, Model, Transcription, History).
  - `src/audio_toolkit/`: Low-level audio processing and VAD.
  - `src/commands/`: Tauri command handlers.
- `src-tauri/resources/models/`: Local storage for ML models.
