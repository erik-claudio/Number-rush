# Number Rush

A free, open-source math practice game for kids. Timed fact sprints, Make 24 puzzles, points, a daily goal and collectible stickers. It's one HTML file with no build step, no backend and no accounts.

## Features

- **Fact Sprint**: Timed rounds with an on-screen keypad and full keyboard support. Earn up to three stars per round. Choose how to practice:
  - **Difficulty**: pick +, −, ×, ÷ or a mix, then a level from 1 to 5.
  - **Grade level**: pick 1st through 5th grade, then a skill aligned to the Texas math standards (TEKS). Third-grade fact skills let you focus on specific times tables.
- **Make 24**: Combine four numbers with + − × ÷ to make exactly 24. Easy uses 1 to 9, hard uses 1 to 13. Every puzzle is checked for a solution before it's shown, and a hint reveals one.
- **Points and daily goal**: Points scale with level, with streak bonuses every five in a row.
- **Stickers**: 12 achievements to unlock.
- **Stats**: Accuracy by operation, best scores by level, longest streak.
- **Multiple players** on one device.

## Run it

Open `index.html` in any modern browser. That's it.

## Publish with GitHub Pages

1. Create a new repository and upload `index.html`, `README.md` and `LICENSE`.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then save.
4. Your game will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Grade-level skills (TEKS)

| Grade | Skills |
| --- | --- |
| 1st | Add within 20, subtract within 20, mixed (1.3D) |
| 2nd | Fast facts within 20 (2.4A), two-digit add and subtract (2.4B), within 1,000 (2.4C) |
| 3rd | Multiplication and division facts to 10 × 10 (3.4F), fact families (3.4J), 2-digit × 1-digit (3.4G), 3-digit add and subtract (3.4A) |
| 4th | × 10 and 100 (4.4B), perfect squares to 15 × 15 (4.4C), 2-digit × 2-digit and 4-digit × 1-digit (4.4D), 4-digit ÷ 1-digit (4.4F), large numbers (4.4A) |
| 5th | 3-digit × 2-digit (5.3B), divide by 2-digit numbers (5.3C), mixed review |

Skills that need scratch paper get longer sprints: 2 minutes for 3-digit work and 3 minutes for multi-digit multiplication and division, with lower star targets to match. All division problems divide evenly.

Facts with 0 and 1 show up less often so practice time goes to the facts kids actually need to learn.

## Customize

The settings live at the top of the script in `index.html`:

| Constant | Default | What it does |
| --- | --- | --- |
| `SPRINT_SECONDS` | `60` | Length of a standard sprint |
| `DAILY_GOAL` | `100` | Points needed to fill the daily bar |
| `STAR_STEPS` | `[10, 20, 30]` | Correct answers needed for 1, 2 and 3 stars in a standard sprint |

Add stickers by appending to the `STICKERS` array. Change difficulty ranges in `gen()`, and add or edit grade-level skills in `SKILLS`. Longer sprints for harder skills are set in `timing()`.

## Data and privacy

Progress is saved in the browser's `localStorage` on the device being used. Nothing is sent anywhere. Clearing browser data resets progress.

## Ideas for contributions

- Teacher view with class codes (would need a backend such as Supabase or Firebase)
- More game modes: missing-number problems, fractions, telling time
- Sound effects and a mute toggle
- Export and import progress

## Disclaimer

Number Rush is an independent project. It is not affiliated with or endorsed by First in Math, Suntex International, or any other math program.

## License

MIT. See [LICENSE](LICENSE).
