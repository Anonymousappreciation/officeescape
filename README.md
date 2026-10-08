# 🔐 OFFICE ESCAPE: THE MYSTERY ROOM

An interactive, educational browser-based escape room game featuring **8 mystery rooms**, dual department paths (**Team A** & **Team B**), animated padlocks, and workplace ethics/logic challenges.

---

## 📁 Project Structure

```
office-escape/
│
├── index.html        # Main HTML game container & UI layout
├── style.css         # Responsive styling & padlock animations
├── script.js         # Complete vanilla JavaScript game engine
│
├── assets/           # Optional custom assets directory
│   ├── images/       # Workplace images & diagrams
│   ├── sounds/       # Sound effects (synthesized via Web Audio API by default)
│   └── videos/       # Optional scenario video clips
│
└── README.md         # Instructions, game mechanics & deployment guide
```

---

## 🎮 Game Concept & Rules

1. **8 Mystery Rooms**:
   - **Room 1: Identifying Values**: Workplace scenario, core value identification, and SOP process questions.
   - **Room 2: Match The Situation**: Match real office events with professional conduct.
   - **Room 3: Office Word Puzzle**: Unscramble foundational workplace pillars (e.g. *TEAMWORK* or *SAFETY*).
   - **Room 4: Emoji Mystery**: Decipher corporate symbolic equations.
   - **Room 5: Office Logic**: Deduce employee arrival sequences using logic clues.
   - **Room 6: Connect The Dots**: Connect coordinates 1 through 8 to forge the golden key.
   - **Room 7: Picture Puzzle**: Reassemble blueprint sectors to discover key hiding spots.
   - **Room 8: The Final Challenge**: Master workplace ethics compliance questions.

2. **Crucial Padlock Rule**:
   - Finding a key alone will **not** unlock the padlock.
   - Solving a challenge alone will **not** unlock the padlock.
   - **Both** `challengeCompleted === true` AND `keyFound === true` are required to pop open the padlock!

3. **Dual Team Modes**:
   - **Team Alpha (Room A)**: Desk sector, wooden drawer, wall calendar, and teamwork focus.
   - **Team Bravo (Room B)**: Executive sector, leather notebook, filing cabinet, and integrity focus.

4. **Self-Contained Sound FX**:
   - Built-in Web Audio API synthesizer for clicks, chimes, buzzers, key discovery, and padlock unlocking.
   - Works offline or online with zero missing audio dependencies.

---

## 🚀 How to Run Locally

### Option 1: Double-Click `index.html`
Simply double-click `index.html` in File Explorer or Finder. The game runs directly in any modern browser!

### Option 2: Run with a Local Server (Recommended)
Using Python:
```bash
# Python 3
python -m http.server 8000
```
Then visit `http://localhost:8000` in your browser.

Using Node.js:
```bash
npx serve .
```

---

## 🌐 How to Deploy to GitHub Pages

1. Create a new GitHub repository named: `office-escape-game`
2. Upload `index.html`, `style.css`, `script.js`, and `README.md`.
3. Open repository **Settings** → **Pages**.
4. Set source to **Deploy from a branch**, select `main`, and root folder `/`.
5. Click **Save**. Within 60 seconds, your game is live!

---

## 🛠️ How to Customize Questions & Content

All content is cleanly organized in `script.js` under the `gameData` object:
- Modify `gameData.teamA` or `gameData.teamB` to change room questions, choices, and clues.
- Adjust timer duration by changing `gameState.timeRemaining = 1200` (in seconds).
- Add new scenarios or change correct answers by updating `correct: 0` index.
