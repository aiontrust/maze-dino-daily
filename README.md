# Dino Daily

A free daily puzzle game for the MAZE DINO – Puzzle Adventures platform. One static page, no server, no build step.

- **Sliding Tiles:** a new dino picture every day, 3×3 or 4×4. Same puzzle for everyone, chosen by date.
- **Mix & Match:** build a hybrid dino from a head, body, tail, color and pattern. Every look is a DNA code like `2-0-1-3-1`, shareable as a link (`#dna=2-0-1-3-1`).
- **Daily challenge:** match two required parts to earn bonus points.
- **Points and streaks:** saved in the browser (localStorage) only.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole game (HTML, CSS, JS, and the SVG dino parts) |
| `logo.svg` | The pink-framed circular maze logo (copy it from the MAZE landing page repo; the page hides the image if it is missing) |

## Publish on GitHub Pages

1. Create a repo named `maze-dino-daily`.
2. Add `index.html` and `logo.svg` to the main branch.
3. In the repo go to Settings → Pages, choose "Deploy from a branch", branch `main`, folder `/ (root)`.
4. The game appears at `https://<your-username>.github.io/maze-dino-daily/`.

## How points work

| Action | Points |
| --- | --- |
| Solve today's 3×3 | 100 + up to 60 for few moves + up to 120 for speed |
| Solve today's 4×4 | 200 + up to 180 for few moves + up to 120 for speed |
| Daily challenge | 50 |
| First award of the day | streak bonus: 5 × streak days, capped at 50 |

Rules: each puzzle size and the challenge pay once per day. Practice puzzles never pay. A day without any award resets the streak.

Points are **not** MAZE tokens and have no cash value. They never touch the blockchain. Keeping them off-chain avoids needing a funded rewards wallet and avoids bot farming.

## Settings

At the top of the script in `index.html`:

```js
const MAZE_DINO_URL = ''; // set to the maze-dino game URL to show a "Tip the dino with MAZE" link
```

## Ideas for later

- Use the DNA code as the on-chain trait data for dino collectibles.
- Share one points and collection store with `maze-dino` by using the same origin or a shared key.
- More challenge types, and weekly themes.
