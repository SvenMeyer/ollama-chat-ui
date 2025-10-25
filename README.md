# Ollama Chat Demo UI

Static HTML interface that talks to a local Ollama instance (`http://localhost:11434`). Features include:

- Model picker fed by `/api/tags`, with active/running model auto-selection and persistence.
- Slash command handling (`/set parameter num_ctx <value>`, `/clear`) that mirrors the CLI behaviour.
- Response telemetry (latency, token counts, context usage) with thousands separators.
- Scrollable transcript area with fixed controls and monospaced layout.

## Quick Start

```bash
python3 -m http.server 8000
# then open http://localhost:8000/ai-chat.html
```

The page bundles everything client-side; no build tooling required.
