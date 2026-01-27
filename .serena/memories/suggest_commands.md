# Suggested Commands: Handy

These commands are used for development, building, and maintaining the Handy project. Use `bun` as the primary package manager.

## Development
- `bun install`: Install frontend and bridge dependencies.
- `bun run tauri dev`: Start the application in development mode with hot-reloading.
- `CMAKE_POLICY_VERSION_MINIMUM=3.5 bun run tauri dev`: Start dev mode on macOS if cmake errors occur.

## Building
- `bun run tauri build`: Build the production-ready application bundle.

## Code Quality
- `bun run lint`: Run ESLint on the frontend code.
- `bun run lint:fix`: Run ESLint and automatically fix issues.
- `bun run format`: Run Prettier for frontend and `cargo fmt` for backend.
- `bun run format:check`: Check formatting without making changes.
- `cargo clippy`: Run Rust linter for backend (run within `src-tauri`).
- `cargo fmt`: Format Rust code (run within `src-tauri`).

## Setup (First-time)
- `mkdir -p src-tauri/resources/models`: Create models directory.
- `curl -o src-tauri/resources/models/silero_vad_v4.onnx https://blob.handy.computer/silero_vad_v4.onnx`: Download required VAD model.
