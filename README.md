# MotionForge

Local-first prompt-to-motion graphics editor. The browser MVP is zero-dependency and includes timeline UI, editable text, scene presets, JSON export, local project storage, media upload, Canvas/WebM export, audio waveform preview, keyframe helpers and optional Ollama integration.

## Run
`python3 -m http.server 4173 --bind 0.0.0.0`

Open http://localhost:4173. For desktop, install Node + Electron dependencies and run `npm install && npm run desktop`.

## Optional local AI
Install Ollama, pull a model (`ollama pull llama3.2`) and run `ollama serve`. MotionForge will try `POST /api/generate` through a local proxy when available, then gracefully fall back to its offline analyzer.

## Roadmap hooks
- Ollama/local LLM: `analyzePrompt()` in index.html
- Canvas renderer/WebM: `renderWebM()`
- Project persistence: localStorage key `motionforge-project`
- Media: FileReader object URLs, waveform analyser
- Desktop shell: electron/main.js
