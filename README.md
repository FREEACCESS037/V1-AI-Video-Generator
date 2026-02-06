# V1 AI

V1 is a simple public AI app with user accounts and an admin panel.

## Features
- User registration and login
- Admin dashboard (user list, enable/disable)
- Chat UI with local model support (Ollama) and optional OpenAI
- Image generation with local Stable Diffusion WebUI
- Video generation (via local VIDEO_API_URL)
- Admin can create users, promote/demote, and save custom Q&A
- All users, chat, and admin knowledge saved to `v1.json`

## Quick start
1. Open a terminal in `D:\Vs Code\V1_AI\server`
2. Install deps: `npm install`
3. Create `.env` from `.env.example` and set `JWT_SECRET`
4. Optional local models:
   - Text: install Ollama and set `OLLAMA_BASE_URL` + `OLLAMA_MODEL`
   - Image: run Stable Diffusion WebUI and set `SD_WEBUI_URL`
   - Video: run your local video server and set `VIDEO_API_URL`
5. (Optional) Set `V1_JSON_PATH` if you want a custom location for `v1.json`
4. Run: `npm run dev`
5. Open `http://localhost:3000`

## Notes
- The first registered user becomes admin automatically.
- If `ADMIN_EMAIL` and `ADMIN_PASSWORD` are set, the server will create that admin on first start.
- If no local model is running, the app will show a friendly message instead of AI responses.
