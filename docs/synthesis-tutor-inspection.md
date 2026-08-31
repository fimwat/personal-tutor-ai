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

## Live lesson: Adding Below Ten
URL: `/exploration/adding_below_ten`

### Lesson shell
- **Top-left controls:** Pause button (`||`) + student name "Thomas" always visible.
- **Equation builder:** three labeled drop zones at top center — `box1 + box2 = box3` — with `+` and `=` symbols between them. These are `AXTextField` elements, so they accept dropped tiles.
- **Instructional prompt:** left side of workspace — *"Click on a tile and drag it into the workspace."*
- **Manipulative tiles:** right-edge vertical palette of colored number tiles, each marked with dots matching their value (red 1, orange 2, yellow 3, green 4/5, light-blue 6, dark-blue 7, purple 8, magenta/pink 9). These are concrete-representation manipulatives, not just numerals.
- **Workspace:** large dashed-grid area on dark starry background where tiles are placed.
- **Actions:** **Clear Workspace** button (bottom right) to reset the attempt.

### Pedagogical pattern
- Lesson type: **"Exploration"** — student constructs the equation by dragging tiles, rather than selecting from multiple choice.
- Scaffolding: equation structure is pre-built (`__ + __ = __`); student only supplies the operands/answer.
- Concrete→abstract: dot-count tiles bridge quantity recognition and symbolic addition.

## Lesson interaction state
- Could not complete a full tutoring turn because the drag-to-box interaction did not visibly register during inspection — likely a precision/timing issue with coordinate-based drag on a canvas-like workspace.
- The lesson structure itself is clear enough to clone: equation scaffold + tile palette + workspace + clear action + audio-first tutor overlay (assumed from Synthesis's audio-first design, not directly observed in this lesson).

## Synthesis vs OpenSchool comparison
| Feature | Synthesis Tutor | OpenSchool |
|---|---|---|
| Auth | Unknown (logged-in session) | Clerk (`clerk.openschool.ai`) |
| Onboarding | Sound check | None observed |
| Dashboard | "Thomas's Progress" + module grid | Lesson queue + subjects |
| Lesson picker | Timeline with themed cards + checkmarks | "Your first 1:1 lesson" card |
| In-lesson UI | Equation builder + drag-drop tile manipulatives | Voice-first chat + manipulatives |
| Manipulatives | Colored dot-count tiles in palette | Base-10 cube piles |
| Lesson type | "Exploration" — construct equation | Socratic 1:1 dialogue |
| Gamification | Arcade button | Streaks + daily goals |
| Pricing | Unknown | $49/$99/$299/week metered |
