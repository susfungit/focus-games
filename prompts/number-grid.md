# Number Grid Focus Test — Game Specification

## Objective
Visually locate numbers **1 through 25 in order** as quickly as possible, without tapping individual numbers.

## Layout
- Display a responsive **5 × 5 grid** containing every integer from 1 to 25 exactly once.
- Shuffle positions for each new grid.
- Use varied, readable number colors against a high-contrast background.
- Keep the entire grid legible on an iPhone without horizontal scrolling.

## Gameplay
1. Generate a randomized grid.
2. Show the instruction **“Scan the grid, then press Start.”**
3. Allow the player to inspect the grid before starting.
4. When Start is pressed, begin a **25-second countdown**.
5. Player scans and counts mentally in ascending order; **do not require tapping the numbers**.
6. At zero, stop the timer and signal that time has ended.
7. Allow the player to record the highest number reached, from 0 to 25.
8. New Grid shuffles the grid and resets the timer and result.

## Controls and feedback
- Start and New Grid controls.
- Optional audible ticking during the countdown and a clear end-of-time sound; audio should respect mobile browser gesture restrictions and allow muting.
- Show time remaining and the reported result.
- Link back to `../index.html`.

## Technical requirements
- Standalone `games/number-grid.html` using HTML, CSS and JavaScript; no backend or external dependencies.
- Use monotonic elapsed-time measurement so backgrounding a phone does not extend the countdown.
- Ensure buttons are touch-friendly and compatible with iPhone Safari, Android and desktop.
- Use relative URLs compatible with GitHub Pages.

## Acceptance criteria
1. Every generated grid contains numbers 1–25 exactly once.
2. The countdown starts only after Start is pressed and ends at 0.
3. The game never requires tapping numbers to progress.
4. New Grid resets all round state and changes the arrangement.
5. Muted mode is fully playable and the end signal works when audio is enabled and permitted by the browser.
