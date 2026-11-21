# Flash Grid Memory — Game Specification

## Objective
Build a standalone, responsive visual working-memory game. Players briefly memorize highlighted cells in a grid, then reproduce the pattern by tapping the original locations.

## Gameplay
1. Player selects difficulty and presses Start / New Round.
2. Random unique grid cells turn blue for a fixed preview period (or indefinitely in Practice).
3. The highlights disappear; the player selects remembered positions.
4. Submit Answer evaluates the selection and reveals correct, missed and extra positions.
5. Start / New Round creates a fresh independent pattern.

## Difficulty
| Mode | Grid | Targets | Preview |
| --- | --- | --- | --- |
| Practice | 5×5 | 5 | Unlimited; Begin Recall manually |
| Easy | 4×4 | 3 | 4 seconds |
| Normal (default) | 5×5 | 5 | 3 seconds |
| Hard | 5×5 | 7 | 2 seconds |
| Expert | 6×6 | 9 | 1.5 seconds |

## Controls
- Start / New Round: regenerate target positions and reset selection.
- Submit Answer: available only during recall; score the selected pattern.
- Clear Selection: remove all selections during recall.
- Show Pattern: reveal answers during recall, marking the round assisted; in untimed Practice preview, the button reads Begin Recall.
- Difficulty selection: enabled between rounds, not during active preview or recall.

## Results
Report correct target cells, missed cells, extra selections, selection precision, and number of perfect unassisted rounds. During review, correct selected targets appear green, missed targets red, and extra selections orange. Assisted reveals are not scored as unassisted perfect rounds.

## Technical Requirements
- One complete `games/flash-grid-memory.html` with inline HTML/CSS/JS, no dependencies.
- Dark, touch-friendly responsive interface, compatible with iPhone Safari and desktop browsers.
- `../index.html` link to return to the Focus Games Hub.
- No backend, no personal data collection; suitable for GitHub Pages.
- Cancel stale preview timers on New Round to prevent overlapping rounds.

## Acceptance Criteria
- Each round has exactly the configured number of distinct targets.
- Targets remain within the grid and cannot be selected during preview.
- The pattern disappears after the configured time.
- Submitting always reveals the true original pattern.
- Starting a new round fully resets prior selections and results.
- Practice mode permits unlimited preview and manual transition to recall.
- Buttons respond to mouse and touch input.
