# Discipline Tracker Pro

Discipline Tracker Pro is a browser-based productivity and sleep tracker designed to help you build consistency, measure output, and sustain momentum over time.

It combines task timing, sleep logging, streak tracking, and competitive self-benchmarking through the **SHADOW Engine**—all with local-first storage and no required backend.

## 🎯 Core Features

### ⏱️ Time & Session Tracking
- Real-time stopwatch for task sessions
- One-click Start/Stop controls
- Dedicated sleep-session logging
- Active task indicator during live sessions
- Auto-save to browser `localStorage`

### 📋 Task Management
- Log tasks with automatic timestamps
- Separate productive sessions from sleep sessions
- Save frequently used tasks as Quick-Start Favorites
- Review same-day task history with durations
- Delete incorrect entries when needed
- Visual category cues (productive vs sleep)

### 📊 Daily Dashboard
- Productive time tracked today
- Sleep time tracked today
- Total tracked time
- Current day streak
- Live metric updates as sessions are logged

### 🔥 Streak System
- Automatic consecutive-day streak counting
- Milestone notifications for key streak moments
- Streak persistence across refreshes and sessions

### 📈 Analytics & Reporting
- Productivity trend chart with multiple ranges (7d, 30d, 3m, 6m, 1y)
- Sleep analysis chart with matching time-range controls
- Monthly report view with summary + daily breakdown
- Export support for CSV and JSON formats

### 💡 Motivation Loop
- Rotating discipline-focused quote system
- Automatic quote transitions every 15 seconds
- Lightweight UI animations to keep focus and momentum

---

## 🌑 SHADOW Engine (Self-Competition System)

The SHADOW Engine turns your historical performance into a daily competitive benchmark.

Your **SHADOW** is your strongest historical 7-day rolling productivity average. Each day, the app compares your current performance against that benchmark so you can measure consistency, not just isolated high-output days.

### How SHADOW Works
- **Shadow Average**: Best historical 7-day rolling average
- **Current Average**: Your real 7-day average right now
- **Gap vs Shadow**: How far ahead or behind you are
- **Today’s Target**: Minimum minutes needed today to stay on pace

### SHADOW Status Bands
- **🟢 Standard Broken**: 100%+ of target
- **🔵 At the Gate**: 90–99%
- **🟡 Trailing**: 70–89%
- **🔴 Out of Range**: <70%

### Rank Tiers
| Tier | Shadow Avg Minutes |
|------|---------------------|
| Initiate | 0+ |
| Builder | 120+ |
| Operator | 180+ |
| Executor | 240+ |
| Elite | 300+ |
| Apex | 360+ |
| Overdrive | 420+ |

### Monthly Competitive Tracking
- My Wins (days you met/exceeded SHADOW)
- Shadow Wins (days SHADOW won)
- Active Days
- Win Percentage

---

## 🎨 UX & Design

- Dark, high-contrast UI theme
- Responsive layouts for desktop, tablet, and mobile
- Motion/transition polish without heavy dependencies
- Semantic structure with accessible visual hierarchy

### Responsive Breakpoints
- **Desktop (1400px+)**: Full layout with all panels
- **Tablet (~768px)**: Stacked single-column sections
- **Mobile (~480px)**: Touch-optimized controls and spacing

---

## 🚀 Quick Start

1. Clone or download this repository.
2. Open `index.html` in your browser.
3. Start tracking immediately—no build step required.

## Usage Flows

### Start a Productive Task
1. Enter a task name.
2. Click **Start** (or press Enter).
3. Let the timer run.
4. Click **Stop** to save the session.

### Log Sleep
1. Click **Sleep**.
2. Run the timer for your sleep session.
3. Click **Stop** to save.

### Add a Favorite Task
1. Enter a common task name.
2. Click the **⭐** button.
3. Reuse it anytime from the Quick-Start list.

### Review Report
1. Click **Report**.
2. Inspect monthly summary and day-level breakdown.
3. Print if needed.

### Export Data
1. Click **Export**.
2. Download CSV or JSON output.

---

## 💾 Data Storage

Data is stored locally in your browser using `localStorage`.

Primary keys:
- `discipline_tracker_tasks`
- `discipline_tracker_favorites`
- `discipline_tracker_streak`
- `discipline_tracker_last_activity`
- `discipline_tracker_active_task`
- `discipline_tracker_shadow_avg`

> Note: clearing browser site data/cache removes stored records.

---

## 🔧 Technical Overview

The app follows a class-oriented, manager-based architecture:

- **DisciplineTracker**: top-level application orchestrator
- **StopwatchManager**: timer lifecycle and session duration logic
- **TaskManager**: task CRUD and history rendering
- **UIManager**: reports, motivational content, and display updates
- **GraphManager**: chart rendering and analytics visuals
- **EventManager**: user input/event wiring
- **ShadowEngine**: rolling-average benchmark logic

See `ARCHITECTURE.md` for structure and migration direction.
