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
