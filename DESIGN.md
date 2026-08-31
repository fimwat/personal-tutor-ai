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

## OpenSchool live lesson details (Multiplication Power-Up)
- Lesson title: **Multiplication Power-Up**
- Strategy taught: **The Split Strategy** — breaks multiplication into place-value chunks:
  - `23 = 20 + 3`
  - `20 × 4 = 80`
  - `3 × 4 = 12`
  - Final prompt: `80 + 12 = ?` (red text = student must complete)
- Explanation sub-step: *"Why 20 × 4 = 80"* with worked chain:
  - `20 = 2 × 10`
  - `2 × 10 × 4`
  - `8 × 10 = 80` (highlighted)
- Tutor controls: **Follow tutor** button + **not sure** fallback link.
- Tutor check-in text: *"Does that make sense, Thomas?"* — personalized by student name.
- Bottom bar: profile icon, chat, pause, audio/speaker, comment icon, mic mute.
- Audio playing indicator in window title confirms voice narration is active.
