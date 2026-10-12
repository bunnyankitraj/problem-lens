# Problem Lens

Submit an idea or a real-world problem and get an AI analysis report back, powered by Google Gemini (free tier).

**Live app:** https://bunnyankitraj.github.io/problem-lens/

## What the report contains
- Sharpened problem statement, who is affected, and scale
- Root causes
- Existing solutions and where they fall short
- Scores out of 10: impact, feasibility, urgency, novelty
- Risks, 3–5 cheap next steps (timeframe + cost), success metrics
- Verdict: **Pursue**, **Refine** or **Park**

## How to use
1. Get a free Gemini API key at https://aistudio.google.com/apikey
2. Open the app, paste the key under **Gemini settings**
3. Describe a problem or idea, press **Analyse**

Your key and saved cases stay in your browser's localStorage. The key is sent only to Google's Gemini API. Nothing is stored on a server.

## Tech
A single static `index.html` (no build step, no backend). It calls the Gemini `streamGenerateContent` endpoint directly from the browser with JSON output mode. Hosted on GitHub Pages.

## Run locally
```bash
python3 -m http.server 8000
```
Then open http://localhost:8000
