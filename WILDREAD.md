# WILDREAD — Student Reading Log & Progress Tracker

Prototype file: `Wildread.dc.html`

## Overview
A student reading log and habit tracker for middle/high school, with a teacher/admin roster view. Blue + yellow wildcat theme, rounded and playful but not babyish. Fully interactive React-based prototype (state, forms, transitions, celebratory micro-interactions) — not a static mockup.

## Onboarding / Auth
- Role picker (Student / Teacher) shown before the app.
- **Student signup:** first name, last name, school year, teacher (dropdown), class/period (dependent dropdown, filtered by chosen teacher). Display name = `First L.`. New student is added to that class's roster with 0 stats.
- **Teacher signup:** name, school year, add/remove classes (periods) to build their roster shell. Finishing creates the teacher and switches into Teacher View for their new class.
- Seeded demo data: Ms. Karen Carpenter (1st Period, 3rd Period) and Mr. James Alvarez (2nd Period), with 8 mock students distributed across them.

## Student-facing screens
1. **Dashboard** — greeting + encouragement line, minutes/books goal gauges (conic-gradient rings), 7-day activity strip, quick actions (Log a Session / Finished a Book / Write a Summary), recently earned badges preview.
2. **Goal Setting** — period picker, minutes/books steppers, teacher-assigned goal shown for comparison.
3. **Log a Session** — book title field, cover via search-by-title/ISBN or photo upload, minutes stepper + optional live timer, date, "I finished this book" checkbox, optional note. Confirmation screen celebrates milestones with a badge-unlock card and full-screen confetti.
4. **Write a Summary** — book picker, 1–5 rating (dot scale), short review text, recommend toggle, plus a browsable journal of past summaries.
5. **My Books** — grid of logged books with cover, status pill (Reading/Finished), minutes, date range; filter by status, sort by recent/title/genre.
6. **Badges** — 17 wildcat/claw/paw-themed badges across 4 categories (First Claws, Wild Streaks, Night Prowls, Den of Books), each with locked/earned states and a detail modal; opening an earned badge also bursts confetti.

## Teacher View
- Report header: "{Teacher name}, {Period}" with a period switcher (only that teacher's classes).
- Class-goal bar chart (per-student horizontal bars vs. goal line) and a sortable/searchable roster table (minutes, books, goal %, badges).
- Clicking a student opens a drill-in panel with their own mini gauges and badge count.

## Visual system
- Primary blue `#2E5FA3`, gold `#FFC933`, teal `#22B8A6`, purple `#8B7CF0`; warm-tinted background `#F5FAFE`.
- Poppins (headings/numbers) + Inter (body). Fully rounded corners, no sharp edges.
- Wildcat mascot mark (simple ears + face) next to the WILDREAD wordmark on every screen.

## Known simplifications (prototype scope)
- All data is in-memory (session only) — no backend/persistence across reloads.
- Cover "search" returns mock placeholder covers keyed to a small local catalog; "upload" uses a drag-and-drop image slot.
- The in-app Student View / Teacher View pill toggle is a demo convenience for reviewing both roles without re-running signup.
