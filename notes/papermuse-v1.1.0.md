# PaperMuse 1.1.0

PaperMuse 1.1.0 expands the macOS research workbench while preserving the release-mode isolation introduced in 1.0.0.

## Highlights

- Adds a reconstructable evidence graph and an evidence-drawer interface for research artifacts.
- Adds versioned, secret-scrubbed run manifests and immutable feedback events with offline replay metrics.
- Improves quality and proximity calibration with pairwise tournament scoring.
- Adds localized legal-interestingness guidance, live card snapshot defaults, and MCII actions for research artifacts.
- Hardens session concurrency, degraded-provider handling, evidence references, manifest scrubbing, and production web UI behavior.

## Platform and setup

- macOS 14 or newer on Apple Silicon.
- The application archive includes the main Python runtime; no source checkout or developer virtual environment is required.
- On first launch, configuration, runtime, results, cache, and logs are stored under `~/Library/Application Support/PaperMuse/`.
- Provider keys remain user-supplied in `~/Library/Application Support/PaperMuse/config/secrets.toml`.

Optional CNKI, zsearch, PaperQA, and gpt-researcher integrations remain explicitly degradable. Paid/API smoke is not run automatically.

## Verification

- Source tag: [`papermuse-v1.1.0`](https://github.com/semantic-craft/paper-muse/tree/papermuse-v1.1.0), commit `7357227f550120b034ae16a92fc9bfc675bbfbd0`.
- Main runtime SHA-256: `1c9afd28b26a1b523c47ad88724e482e4332c881910f5acf791fa4cc80a43e79`.
- `PaperMuse-macos-arm64.zip` SHA-256: `daf89c0af2ef0870655c2d361cb07d116eb8a403cce956b7864d30fd5b6b60bb`.
- Apple notarization submission `7fa36132-aae0-4829-9feb-1b51fb0a1954` was accepted.
- The zipped app passed strict code-signature verification, staple validation, and Gatekeeper assessment as a notarized Developer ID application.
