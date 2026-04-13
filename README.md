# 🔍 QALingo

> *"QAlemental, Dear Watson."*

**The Duolingo-style learning platform for QA professionals.**
Learn testing fundamentals, crush your ISTQB exam, ace your interviews — 5 minutes a day.

---

## What Is QALingo?

QALingo is a gamified web application that helps QA professionals at any level learn, certify, and get hired — with the same daily habit loop that makes Duolingo addictive.

Built by a QA professional with 10+ years of experience and ISTQB certification. Every question, scenario, and explanation comes from real-world testing practice.

**Target user:** Latin American QA professionals breaking into international remote roles.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5 · CSS3 · Vanilla JavaScript |
| AI Feedback | Anthropic Claude API (Interview Prep) |
| Database (planned) | Supabase |
| App Builder (planned) | Bubble.io |
| Email (planned) | Loops.so |
| Hosting (planned) | Netlify / GitHub Pages |

No frameworks. No build tools. Every file opens directly in a browser.

---

## Modules Built

### 1. 🌐 Landing Page — `qalingo-landing.html`
Waitlist capture page with full product overview.
- Hero section with Q mascot and waitlist form
- Feature showcase (6 learning levels, ISTQB simulator, Interview Prep)
- Curriculum preview and social proof
- Connects to Loops.so for email capture

### 2. 🚀 Onboarding Flow — `qalingo-onboarding.html`
7-screen personalized path builder.
- Experience level selector (Beginner → Senior)
- Goal picker (Get hired / Certify / Upskill / Explore)
- Daily commitment and reminder time
- Dynamic path generation based on user answers
- Saves profile to localStorage (Supabase in production)

### 3. 🎮 Lesson App — `qalingo-lesson-app.html`
Interactive ISTQB Foundation Chapter 1 experience.
- 9 screens: concept cards + 3 exercise types
- Multiple choice with per-answer explanations
- "Is This a Bug?" binary scenarios
- Fill-in-the-blank terminology
- XP system, hearts, streak counter, Q feedback messages

### 4. 🎯 ISTQB Exam Simulator — `qalingo-istqb-simulator.html`
Full 40-question mock exam mirroring the real ISTQB CTFL v4.0 format.
- 40 questions across 6 chapters
- 60-minute countdown timer
- Question map with answered/flagged/wrong status
- Immediate answer explanation after each selection
- Detailed report: score, pass/fail (65%), chapter breakdown, full review

### 5. 💼 Interview Prep — `qalingo-interview-prep.html`
AI-powered drip interview practice with Claude feedback.
- 3 levels: Junior / Mid-Level / Senior QA
- 2 modes: Daily Drip (1 question + full AI feedback) and Simulation (5 questions timed)
- AI evaluates structure, depth, and clarity with scores
- Strengths, improvements, and model answer per response
- Streak persistence via localStorage

### 6. 🏆 Gamification Dashboard — `qalingo-gamification.html`
Full progress and rewards system.
- XP level progression (Level 1–10+)
- 23-day streak calendar with visual history
- 28 badges (14 unlocked / 14 locked) with unlock animations
- Weekly XP bar chart
- Achievements-in-progress with progress bars
- Global leaderboard + league leaderboard
- Daily challenge with confetti reward
- Badge popup with LinkedIn share prompt

### 7. 📋 Architecture Document — `qalingo-architecture.html`
Complete product blueprint.
- User journey (6 steps)
- 6-level curriculum map with lesson counts
- Exercise type definitions
- Q's voice and gamification system
- Monetization model (Free / Pro $12/mo / Teams $8/seat)
- 6-week MVP timeline
- Success metrics and recommended tech stack

---

## File Structure

```
qalingo/
├── qalingo-landing.html          # Public landing page + waitlist
├── qalingo-onboarding.html       # New user onboarding flow
├── qalingo-lesson-app.html       # ISTQB Ch.1 interactive lesson
├── qalingo-istqb-simulator.html  # 40-question exam simulator
├── qalingo-interview-prep.html   # AI-powered interview practice
├── qalingo-gamification.html     # Progress, badges, leaderboard
├── qalingo-architecture.html     # Full product blueprint
├── qalingo-backend-guide.html    # Supabase + Bubble setup guide
└── README.md                     # This file
```

---

## How to Run

No installation required. Every file is self-contained.

```bash
# Option 1: Open directly in browser
open qalingo-landing.html

# Option 2: Local server (recommended)
npx serve .
# then visit http://localhost:3000

# Option 3: Deploy instantly (free)
# Drag any file to netlify.com/drop
```

**Interview Prep AI feedback** requires a Claude API key.
Add it to the fetch header in `qalingo-interview-prep.html` → `submitAnswer()` function.

---

## MVP Success Metrics

| Metric | Target |
|--------|--------|
| Day 3 return rate | ≥ 30% |
| Waitlist signups pre-launch | 100 |
| Free → Pro conversion (90 days) | ≥ 5% |
| Avg streak at Week 4 | ≥ 7 days |

---

## Roadmap

- [x] Landing page with waitlist
- [x] Onboarding flow (7 screens)
- [x] ISTQB Module 1 — Fundamentals of Testing
- [x] ISTQB Exam Simulator (40 questions, 6 chapters)
- [x] Interview Prep with AI feedback (3 levels)
- [x] Gamification system (XP, badges, streaks, leaderboard)
- [ ] Supabase backend (auth + database)
- [ ] Bubble.io app integration
- [ ] Loops.so email automation
- [ ] ISTQB Modules 2–6 content
- [ ] Scrum Foundation module
- [ ] Stripe payment integration (Pro plan)
- [ ] Mobile app (React Native)

---

## Business Model

| Plan | Price | Includes |
|------|-------|---------|
| Free | $0 | Levels 0–1 · 5 hearts/day · 3 interview Qs/week |
| Pro | $12/mo | All 6 levels · unlimited hearts · full exam simulator · daily interview drip |
| Teams | $8/seat/mo | Pro + team dashboard · custom paths · admin controls |

---

## Content Philosophy

Every question was written by a QA professional who has:
- Worked across web, mobile, API, and CI/CD testing
- Held ISTQB Foundation certification
- Interviewed for and at international remote companies
- Built QA processes from scratch in Agile teams

This is not AI-generated filler. Every explanation answers: *"Why did I get this wrong, and what should I actually remember?"*

---

## Q — Your Detective Guide

Q is the blue bug detective with a magnifying glass. Sharp, occasionally snarky, always in your corner.

```
✅ Correct    → "QAlemental, Dear Watson."
❌ Wrong      → "Even the best detectives miss clues. Try again."
🔥 7-day str  → "A true QA detective never misses a day."
💀 Str lost   → "The bug got away... this time."
🏆 Module ✓   → "Case closed. On to the next one."
💼 Job ready  → "QAlemental, Dear Watson. They'll hire you on the spot."
```

---

*Built with HTML, CSS, and JavaScript. No frameworks. No excuses.*
*QALingo — Learn QA. Get Certified. Get Hired.*
