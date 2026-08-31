# Design
## Stack (TBD, recommend Vite + React SPA)
- Frontend: Vite + React (mirrors OpenSchool `/app`).
- Tutor API: FastAPI/Node, server-side LLM (Nous Portal + Claude fallback).
- Voice: Web Speech API (browser-native) + eSpeak/meSpeak WASM for phoneme clips.
- Auth: Clerk (10 min drop-in) or stub for MVP.
- Progress/streaks: SQLite/Postgres via lightweight API.
- Deploy: Vercel (easiest) or S3+CloudFront like OpenSchool.

## Product flow (from OpenSchool inspection)
1. Diagnostic → scope-and-sequence by topic.
2. Warm-up with concrete manipulatives (e.g., base-10 cube piles for multiplication).
3. Socratic tutor: asks, checks, never hands over answer.
4. Voice-first, text fallback toggle.
5. Streaks + weekly progress email.
