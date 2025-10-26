# Ollama Chat Demo UI

Static HTML interface that talks to a local Ollama instance (`http://localhost:11434`). Features include:

- Model picker fed by `/api/tags`, with active/running model auto-selection, persistence, and per-model context hydration.
- Live context window detection via `/api/show` (fallback `/api/ps`), plus whole-conversation context tracking when streaming through `/api/generate`.
- Consistent telemetry bars that surface per-turn latency, token counts, context usage percentages, and throughput (tok/s), alongside an aggregated footer view.
- Clipboard helpers for copying the full transcript or the latest prompt/response pair.
- Scrollable transcript area with fixed controls, monospaced layout, and stacked send/copy buttons sized to the input field.

## Quick Start

```bash
cd public
python3 -m http.server 8000
# then open http://localhost:8000/ai-chat.html
```

The page bundles everything client-side; no build tooling required.
