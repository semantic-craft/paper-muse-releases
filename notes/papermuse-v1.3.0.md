# PaperMuse 1.3.0

PaperMuse 1.3.0 lets you choose your LLM provider — DeepSeek, OpenAI, or Gemini — directly on the first-run screen, building on the in-app key setup added in 1.2.0.

## Highlights

- **Choose your LLM provider in-app**: the first-run screen now has a DeepSeek / OpenAI / Gemini selector plus a key field for the chosen provider. First-run setup is no longer locked to DeepSeek — any one LLM provider key (plus a Tavily retrieval key) is enough.
- The selected provider is persisted as the roundtable default, so the main flow uses whichever provider you configured. Scan already auto-detects configured providers.
- Keys are written only to the local `secrets.toml` and are never uploaded.

## Platform and setup

- macOS 14 or newer on Apple Silicon.
- The application archive includes the main Python runtime; no source checkout or developer virtual environment is required.
- On first launch, configuration, runtime, results, cache, and logs are stored under `~/Library/Application Support/PaperMuse/`.
- Provider keys can be entered in-app on the first-run screen, or placed in `~/Library/Application Support/PaperMuse/config/secrets.toml`.

Optional CNKI, zsearch, PaperQA, and gpt-researcher integrations remain explicitly degradable. Paid/API smoke is not run automatically.

## Verification

- Source tag: [`papermuse-v1.3.0`](https://github.com/semantic-craft/paper-muse/tree/papermuse-v1.3.0), commit `9fd34f0d7835158a08452ee23047f3ff515724b4`.
- Main runtime SHA-256: `1c9afd28b26a1b523c47ad88724e482e4332c881910f5acf791fa4cc80a43e79`.
- `PaperMuse-macos-arm64.zip` SHA-256: `07a4cd350301abd2ad522ca14bb2e85299fd6f149be00ef2dca743b7eee17721`.
- Apple notarization submission `f19bb187-61cb-4d00-a9cf-849ff40adcd4` was accepted.
- The zipped app passed strict code-signature verification, staple validation, and Gatekeeper assessment as a notarized Developer ID application.
