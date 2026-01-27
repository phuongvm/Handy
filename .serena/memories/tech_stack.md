# Tech Stack & Conventions: Handy

## Technology Stack
- **UI**: React 18, TypeScript, Tailwind CSS (v4).
- **State Management**: Zustand (frontend), Tauri State (backend).
- **I18n**: i18next (strict enforcement, no hardcoded strings in JSX).
- **Backend**: Rust (Tauri 2.x).
- **Inference**: GGML/Whisper.cpp (via `whisper-rs`), ONNX (via `vad-rs`).

## Code Style & Conventions

### Backend (Rust)
- **Error Handling**: Handle errors explicitly; avoid `unwrap()` or `expect()` in production code. Use `Result`.
- **Naming**: standard Rust `snake_case`.
- **Organization**: Follow the Manager Pattern (e.g., `AudioManager`, `TranscriptionManager`).
- **Formatting**: `cargo fmt` is mandatory.

### Frontend (React/TS)
- **Components**: Functional components with hooks.
- **Types**: Strict TypeScript; avoid `any`.
- **Styles**: Use Tailwind CSS utility classes.
- **I18n**: Use `t('key.path')`. Ensure keys are added to `src/i18n/locales/en/translation.json` first.
- **Path Aliases**: Use `@/` to refer to the `./src/` directory.

### Commit Messages
- Use Conventional Commits: `feat:`, `fix:`, `docs:`, `refactor:`, `chore:`.
