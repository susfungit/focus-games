# Track the Ball — Game Specification

## Objective
Keep visual attention on a target ball as it changes from red to white, blends in with other balls, then returns to red.

## Layout and movement
- Large black circular playing area with many small balls.
- One target ball begins red; other balls are white.
- Balls move continuously in varying directions, bounce off the circular boundary, and can collide with each other.
- Motion should be fluid and reasonably fast, with no jitter or teleportation.
- Keep all balls within the play area and avoid visible markers that reveal the target while white.

## Target color sequence
1. Target starts visibly red, allowing the player to identify it.
2. Red gradually fades to white.
3. Target remains fully white and indistinguishable from the others for approximately **15 seconds**.
4. Target gradually returns to red, allowing the player to check whether they tracked it correctly.

Use configurable transition durations, and document the chosen defaults in the implementation. Do not abruptly change the target's position when its color changes.

## Controls and difficulty
- Start, Pause/Resume and Reset/New Round.
- Provide adjustable ball count and movement speed. If updating an existing implementation, preserve its current options unless explicitly requested otherwise.
- Display a clear instruction: track the red ball even while it is white.
- Provide a link back to `../index.html`.

## Technical requirements
- Implement as standalone `games/track-the-ball.html` using HTML, CSS and JavaScript.
- Use time-based `requestAnimationFrame` animation and reliable circle-boundary handling.
- Responsive to iPhone Safari, Android and desktop, including touch controls.
- No backend or external dependencies; use relative links for GitHub Pages.

## Acceptance criteria
1. Only the target ball changes color; all others remain white.
2. The target's white phase lasts approximately 15 seconds.
3. Motion continues smoothly through both fades and the white phase.
4. All balls remain inside the circular play area.
5. Start, Pause and Reset work reliably on mobile.

## Notes
This specification captures the established game concept. Exact ball-count and speed choices should be checked against the current HTML file before making changes.
