# PaperMuse 1.2.0

PaperMuse 1.2.0 adds in-app first-run key setup, so provider keys can be entered directly in the application instead of hand-editing `secrets.toml`.

## Highlights

- **In-app first-run key setup**: paste DeepSeek and Tavily API keys directly on the first-run screen and click 保存并检查 — no manual `secrets.toml` editing. Keys are written only to the local `secrets.toml` and are never uploaded.
- Adds a local-only `POST /setup/secrets` engine endpoint that writes provider keys to the correct config path (dev or release), auto-completes `ENCODER_API_TYPE`, and re-reports setup state. Missing encoder keys still degrade gracefully without blocking startup.

## Platform and setup

- macOS 14 or newer on Apple Silicon.
- The application archive includes the main Python runtime; no source checkout or developer virtual environment is required.
- On first launch, configuration, runtime, results, cache, and logs are stored under `~/Library/Application Support/PaperMuse/`.
- Provider keys can be entered in-app on the first-run screen, or placed in `~/Library/Application Support/PaperMuse/config/secrets.toml`.

Optional CNKI, zsearch, PaperQA, and gpt-researcher integrations remain explicitly degradable. Paid/API smoke is not run automatically.

## Verification

- Source tag: [`papermuse-v1.2.0`](https://github.com/semantic-craft/paper-muse/tree/papermuse-v1.2.0), commit `187417464f95bcd76159a2d150d35ae4b6715ec5`.
- Main runtime SHA-256: `1c9afd28b26a1b523c47ad88724e482e4332c881910f5acf791fa4cc80a43e79`.
- `PaperMuse-macos-arm64.zip` SHA-256: `68c9f83e24f76ba435c4e6f48946a27a60bacd5b74b3046c3d750299422c1596`.
- Apple notarization submission `900c1aaa-9160-45d9-8f36-d8484e6d20d9` was accepted.
- The zipped app passed strict code-signature verification, staple validation, and Gatekeeper assessment as a notarized Developer ID application.
