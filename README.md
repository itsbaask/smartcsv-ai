# SmartCSV AI

A polished CSV analysis workspace with local data profiling and optional AI-powered insights through OpenRouter.

## Features
- Responsive dashboard and CSV drag-and-drop upload
- CSV preview, column type detection, missing-cell and duplicate checks
- Completeness score and sample dataset
- AI analysis through a server-side OpenRouter endpoint
- API keys stay on the server; no key is included in frontend files

## Run locally
1. Install Node.js 18 or newer.
2. Run `npm install`.
3. Set `OPENROUTER_API_KEY` in your shell/environment (optional until AI analysis is used).
4. Optionally set `OPENROUTER_MODEL` to your preferred model.
5. Run `npm start` and open `http://localhost:3000`.

## Render deployment
Create a **Web Service** from this repository. Use build command `npm install` and start command `npm start`. Add `OPENROUTER_API_KEY` and optionally `OPENROUTER_MODEL` under Render Environment. Do not commit secrets or put keys in browser code.

The default AI model is `openai/gpt-4o-mini`; choose any model available to your OpenRouter account via the environment variable.

## Notes
CSV content is parsed in the browser for preview and profiling. When you request AI analysis, column names and up to 30 rows are sent to the server and then to the configured OpenRouter model. Avoid uploading sensitive data unless you are comfortable sending that sample to your chosen AI provider.
