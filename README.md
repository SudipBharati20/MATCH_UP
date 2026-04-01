# ⚽ FIFA SIM — Top 5 Leagues Match Simulator

A browser-based football match simulator using real FC 26 player ratings from the Top 5 European Leagues.

---

## 📁 Project Structure

```
fifa-sim/
├── index.html          ← Main entry point (open this in browser)
├── css/
│   └── style.css       ← All styles (Inter Milan dark theme)
└── js/
    ├── data.js         ← All teams, players, FC 26 ratings
    ├── engine.js       ← Match simulation logic
    └── app.js          ← UI controller & screen management
```

---

## 🚀 How to Run

### Option A — Just open the file (simplest)
Double-click `index.html` — it works with no server needed.

### Option B — VS Code Live Server (recommended)
1. Install the **Live Server** extension in VS Code
2. Right-click `index.html` → **Open with Live Server**
3. Opens at `http://127.0.0.1:5500`

---

## 🎮 Game Modes

### Single Player
- You pick a team
- CPU randomly picks an opposing team
- 90-minute match simulated in real-time (60 seconds)
- Live commentary + stats + player ratings at full-time

### Multiplayer (Hot-Seat)
- Player 1 picks their team
- Player 2 picks their team
- Same simulation, both on the same device

---

## 🏆 Teams Included (FC 26 Ratings)

| League        | Teams                                          |
|---------------|------------------------------------------------|
| Premier League | Man City, Arsenal, Liverpool, Chelsea          |
| La Liga        | Real Madrid, Barcelona, Atlético Madrid        |
| Serie A        | Inter Milan, Juventus                          |
| Bundesliga     | Bayern Munich, Borussia Dortmund               |
| Ligue 1        | PSG, Monaco                                    |

---

## ⚙️ How to Add More Teams

Open `js/data.js` and add a new entry to the `TEAMS` object following the existing pattern:

```js
your_team: {
  id: "your_team",
  name: "Your Team Name",
  league: "premierLeague",   // Must match a key in LEAGUES
  color: "#HEX",
  color2: "#HEX",
  rating: 85,
  formation: "4-3-3",
  players: [
    { id:"unique_id", name:"Player Name", pos:"ST", rating:88,
      pace:85, shooting:90, passing:70, dribbling:80, defending:40, physical:80 },
    // ... 11 players total (1 GK + 10 outfield)
  ]
}
```

**Position codes:** GK, CB, RB, LB, RWB, LWB, CDM, CM, CAM, LM, RM, RW, LW, ST

---

## 🔧 Customization

| File | What to change |
|------|---------------|
| `js/data.js` | Add teams, edit player ratings |
| `js/engine.js` | Tweak simulation formulas, goal rates, commentary |
| `css/style.css` | Colors, fonts, layout |
| `index.html` | Add new screens or UI elements |

---

## 📌 Notes
- No dependencies, no npm, no build step — pure HTML/CSS/JS
- Works in any modern browser (Chrome, Firefox, Edge, Safari)
- Match simulation is randomized but weighted by real FC 26 ratings
