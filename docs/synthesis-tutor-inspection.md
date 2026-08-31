# Synthesis Tutor inspection notes
Source: live Edge session, `tutor.synthesis.com`, student account "Thomas".

## Onboarding
- Sound-check gate: *"Let's do a quick sound check."* → plays audio → *"Can you hear the music?"* → **Yes** / *"Not working?"* fallback.
- Audio-first assumption built in from first interaction.

## Dashboard
- Heading: **"Thomas's Progress"**.
- Prompt: *"Pick a unit to jump into."*
- Module grid: 8 circular unit buttons — Place Value, Addition, Subtraction, Multiplication, Division, Fractions, Bonus Lessons, Flashcards.
- Module outline color = progress state: teal/green = started, blue = untouched/available. Flashcards had a partial blue ring (progress indicator).
- Persistent **Arcade** button (bottom center) — gamification always one tap away.
- Top-left: **Pause** button + student name always visible.

## Lesson timeline
- Entering a module shows a timeline of themed lesson cards with **green completion checkmarks**.
- Sidebar: *"Choose a lesson from the timeline."* + **Go Back** button.
- Fractions module example titles: *Share the Cookies, Same Amount of Cookie, Slicker Slicing, Cookies and Crumbs, Whole Lot of Pieces, Fractions out of Line, Fractions Intro, We Need Fractions, The Bottom Number, The Top Number, Fractions Practice, Painting Fractions, Reading Fractions, Unequal Pieces, What's Equivalent?, Intro to Equivalent Fractions, Like a half, Halfway Certain, Like two thirds, Equivalent Fraction Practice, Painting Equivalent Fractions, Split Decisions, One Third Plus One Third, A Half and an Eighth*.
- Lesson cards: thumbnail image + title; completed = green checkmark overlay.
- Bottom row cards had no visible checkmark in the inspected state (likely incomplete/available).

## Lesson interaction (NOT yet observed)
- Could not enter an actual in-progress lesson: all top-row Fractions lessons were marked complete, and clicking bottom-row cards did not visibly transition to a lesson shell during inspection.
- Need: a fresh/less-progressed account, or direct lesson URL, to observe the real tutoring turn.

## Synthesis vs OpenSchool comparison
| Feature | Synthesis Tutor | OpenSchool |
|---|---|---|
| Auth | Unknown (logged-in session) | Clerk (`clerk.openschool.ai`) |
| Onboarding | Sound check | None observed |
| Dashboard | "Thomas's Progress" + module grid | Lesson queue + subjects |
| Lesson picker | Timeline with themed cards + checkmarks | "Your first 1:1 lesson" card |
| In-lesson UI | Not yet observed | Voice-first chat + manipulatives |
| Gamification | Arcade button | Streaks + daily goals |
| Pricing | Unknown | $49/$99/$299/week metered |
