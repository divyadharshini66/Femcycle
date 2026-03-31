# 🌸 FemCycle — Women Health Cycle Predictor

A modern, fast, and premium React web app for predicting menstrual cycles with smart health insights.

---

## Features

- **Cycle Prediction** — Next period date, ovulation day, fertile window, and safe days
- **Phase Detection** — Identifies your current phase (Period / Follicular / Ovulation / Luteal)
- **Cycle Calendar** — 42-day color-coded calendar view
- **Timeline Chart** — Visual bar breakdown of your full cycle
- **Smart Health Tips** — Diet, exercise, and health advice tailored to your current phase
- **Mood Tracker** — Log your daily mood
- **Symptoms Tracker** — Track cramps, bloating, fatigue, and more
- **Reminder** — Set a reminder for your next period
- **Multi-language** — English, Tamil (தமிழ்), Hindi (हिंदी)

---

## Tech Stack

- [React 18](https://react.dev/)
- [Vite 5](https://vitejs.dev/)
- Pure CSS (no UI library — keeps it fast and lightweight)

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS version recommended)

### Install & Run

```bash
cd femcycle
npm install
npm run dev
```

Open your browser at `http://localhost:5173`

### Build for Production

```bash
npm run build
```

Output goes to the `dist/` folder — ready to deploy on Netlify, Vercel, or GitHub Pages.

### Preview Production Build

```bash
npm run preview
```

---

## Project Structure

```
femcycle/
├── index.html              # HTML entry point
├── package.json
├── vite.config.js
└── src/
    ├── main.jsx            # React root
    ├── App.jsx             # Main app, state management
    ├── i18n.js             # All translations (EN / TA / HI)
    ├── tips.js             # Health tips per cycle phase
    ├── utils.js            # Date helpers & cycle calculations
    ├── index.css           # Global styles
    └── components/
        ├── Header.jsx      # Sticky header + language switcher
        ├── InputForm.jsx   # User input form + symptom chips
        ├── ResultCards.jsx # 4 result cards + phase banner
        ├── CycleCalendar.jsx # Color-coded 42-day calendar
        ├── Timeline.jsx    # Horizontal cycle timeline chart
        ├── HealthTips.jsx  # Phase-based tips grid
        └── Reminder.jsx    # Next period reminder
```

---

## How It Works

1. Enter your last period date, average cycle length, and period duration
2. Optionally log your mood and symptoms
3. Click **Predict My Cycle**
4. View your next period, ovulation day, fertile window, safe days, and personalized health tips

### Cycle Calculation Logic

| Phase | Days |
|---|---|
| Period | Day 1 → periodDuration |
| Follicular | After period → ~Day (cycleLen - 19) |
| Fertile Window | 5 days before ovulation |
| Ovulation | cycleLen - 14 |
| Luteal | After ovulation → next period |

---

## Supported Languages

| Language | Code |
|---|---|
| English | `en` |
| Tamil | `ta` |
| Hindi | `hi` |

---

## License

MIT — free to use and modify.
