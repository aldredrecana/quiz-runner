# 🏃 Quiz Runner

A kid-friendly endless runner (Subway Surfers style) where players run into the lane with the **right answer** to quiz questions.
Runs in any browser, no install, no backend. Hosted free on GitHub Pages.

## How to play
- **Move lanes:** swipe left/right, tap the ◀ ▶ buttons, or use ← → (A / D)
- **Jump** over crates and cones: swipe up, tap anywhere, tap ▲, or press ↑ / W / Space
- **Slide** under orange bars: swipe down, tap ▼, or press ↓ / S
- **Quiz gates:** read the question at the top, then run into the lane with the right answer (A, B or C)
- **Pickups:** 🪙 coins = points, 🛡️ shield saves you once, ⏳ slow-mo gives more time
- **Streaks:** 3 right answers in a row = an extra heart ❤️
- **P** / Esc pauses, **M** mutes

## Menu options
- **Subject:** Math, Filipino, English, Science, Pilipinas, or Mixed
- **Level:** Grades 1-2, 3-4, 5-6
- **Speed:** Chill 🐢, Normal 🏃, Fast ⚡ (the game always starts slow and speeds up; questions always slow the road so there is time to read)
- Best score is saved separately for every subject + level + speed combination

## Adding your own questions
Edit `questions.json` (no code needed). Each question looks like this:

```json
{ "cat": "science", "level": 2, "q": "Water freezes into?", "answer": "ice", "wrong": ["steam", "sand"] }
```

- `cat`: `filipino`, `english`, `science` or `ph` (Math questions are generated automatically)
- `level`: `1`, `2` or `3`
- `wrong` needs exactly two wrong answers, and all three answers must be different
- Invalid entries are skipped automatically, so a typo can never break the game
- Keep at least ~12 valid questions in the file, otherwise the built-in questions are used instead

## Deploy on GitHub Pages
1. Put `index.html` and `questions.json` at the top level of the repo
2. Settings → Pages → Deploy from a branch → `main` / `/ (root)` → Save
3. Open `https://YOUR-USERNAME.github.io/REPO-NAME/`

## Optional: real artwork
Put transparent PNGs in a `sprites/` folder named `player`, `ob`, `low`, `coin`, `shield`, `slow`, then set `USE_SPRITES = true` in `index.html`. Missing images fall back to the built-in drawings.

## Roadmap ideas
- Unlockable characters and hats bought with coins
- Teacher mode: pick custom question sets / print a results report
- More subjects (Social Studies, Values Education) and Filipino-English word games
- Daily challenge and weekly star goals
- Installable offline app (PWA)
