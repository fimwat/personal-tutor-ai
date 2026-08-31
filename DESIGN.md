# Design
## Competitors inspected
- **OpenSchool** (`openschool.ai`) — voice-first Socratic tutor, cube-block manipulatives, Clerk auth, AWS S3+CloudFront, weekly-time metered SaaS.
- **Synthesis Tutor** (`tutor.synthesis.com`) — sound-check onboarding, themed lesson timelines ("Share the Cookies", "Slicker Slicing"), dashboard = "Thomas's Progress", Arcade gamification button, dark space theme, audio-first with pause controls, completed-lesson checkmarks.

## Stack (TBD, recommend Vite + React SPA)
- Frontend: Vite + React (mirrors OpenSchool `/app`).
- Tutor API: FastAPI/Node, server-side LLM (Nous Portal + Claude fallback).
- Voice: Web Speech API (browser-native) + eSpeak/meSpeak WASM for phoneme clips.
- Auth: Clerk (10 min drop-in) or stub for MVP.
- Progress/streaks: SQLite/Postgres via lightweight API.
- Deploy: Vercel (easiest) or S3+CloudFront like OpenSchool.

## Product flow (observed)
1. **Sound check onboarding** — verify audio before first lesson (Synthesis pattern).
2. Dashboard: **"Student's Progress"** with module grid (math topics) + **Arcade** rewards button.
3. Lesson timeline: themed cards with completion checkmarks, "Choose a lesson from the timeline."
4. Warm-up with concrete manipulatives (OpenSchool: base-10 cube piles; Synthesis: cookie/slicing metaphors).
5. Socratic tutor: asks, checks, never hands over answer (OpenSchool confirmed live).
6. Voice-first, text fallback toggle (both products).
7. Streaks + weekly progress email.
