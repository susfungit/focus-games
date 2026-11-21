# Odd Marble — Game Specification

## Objective
Identify the one marble rotating anticlockwise among otherwise identical clockwise-moving marbles.

## Layout and mechanics
- Use a large black circular playing field.
- Each marble follows its **own small, fixed circular orbit**; orbit centers never move.
- Exactly one marble rotates anticlockwise; every other marble rotates clockwise.
- All marbles are visually identical until the user requests a hint; keep orbit guides invisible.
- Motion must be smooth, continuous and circular, with no lateral drifting, bouncing or sudden direction changes.
- Randomize fixed orbit positions and initial phases each round, keeping complete orbits within the playing field and minimizing overlap.

## Difficulty and speed
- Marble counts: **50, 60, 70**; default **50**.
- Speeds: Slow, Normal, Fast; default **Normal**.
- Normal is the former Fast speed; Fast is faster still. Keep all marbles at the same angular speed magnitude.
- Changing speed should take effect without restarting the round.

## Controls and feedback
- Start / New Round: choose exactly one reverse-moving marble and begin animation.
- Pause / Resume: preserve marble positions.
- Show Odd Marble / Hide Odd Marble: color the reverse marble orange while preserving its motion; restore white when hidden.
- Tap/click to choose a marble; give clear correct/incorrect feedback without requiring precise mouse-only interaction.
- Provide a way to return to `../index.html`.

## Technical requirements
- Standalone `games/odd-marble.html` with HTML, CSS and JavaScript; no backend or external dependencies.
- Use `requestAnimationFrame` with time-based angular updates; account for resize and device pixel ratio.
- Responsive touch-friendly controls for iPhone Safari, Android and desktop.
- Static hosting compatible with GitHub Pages; use relative URLs.

## Acceptance criteria
1. Exactly one marble rotates anticlockwise at any time during an active round.
2. Every marble follows a fixed circular orbit, even after resizing.
3. The Show/Hide control always identifies the true reverse marble.
4. All 50/60/70 settings and all speeds work.
5. Start, Pause, Show and selection work by touch on iPhone Safari.
