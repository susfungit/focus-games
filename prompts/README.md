# Focus Games — Prompt Specifications

This directory contains the intended behavior for each game in the Focus Games Hub.

| Specification | Implementation |
|---|---|
| `odd-marble.md` | `../games/odd-marble.html` |
| `track-the-ball.md` | `../games/track-the-ball.html` |
| `number-grid.md` | `../games/number-grid.html` |

## Updating a game with an AI coding assistant

Use a prompt such as:

> Read `prompts/<game-name>.md` and `games/<game-name>.html`. Make the requested change while preserving all other documented behavior. Verify touch interactions and mobile layout. If requirements change, update the corresponding Markdown specification and summarize the differences.

Specifications describe desired behavior, not a guarantee that the current HTML implements every detail. Review the current implementation and test it before publishing changes.

## Repository conventions
- Keep each game as a standalone HTML file in `games/`.
- Keep the landing page in `index.html`.
- Use relative paths for navigation.
- Commit specifications alongside corresponding code changes.
- Rely on Git history for versions rather than copying numbered prompt files.
