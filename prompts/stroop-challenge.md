# Stroop Color Challenge — Game Specification

## Objective
Players identify the **ink color** of a displayed color word, ignoring its semantic meaning. This exercises selective attention and response inhibition.

## Gameplay
1. Player chooses difficulty and optionally enables sound.
2. Press **Start / New Round** to begin.
3. A color word appears, sometimes written in a conflicting ink color.
4. Player taps the button corresponding to the **ink color**, not the word.
5. Brief correct/incorrect feedback is displayed for **300 ms**.
6. The next stimulus appears **automatically**. **Never include a Next button.**
7. When the timer ends, display results. Practice mode is untimed.

## Difficulty
| Mode | Colors | Time | Approximate conflicting trials |
|---|---:|---:|---:|
| Practice | 5 | Untimed | 65% |
| Easy | 3 | 60 sec | 45% |
| Normal (default) | 5 | 45 sec | 70% |
| Hard | 5 | 30 sec | 90% |
| Expert | 6 | 30 sec | 100% |

Colors: Red, Blue, Green, Yellow, Purple, Orange. Avoid repeating the same word consecutively.

## Controls
- Start / New Round
- Pause / Resume: pause timer, hide stimulus; resume fairly
- Difficulty selector
- Sound On/Off
- Large touch-friendly ink-color answer buttons

## Results
Correct, incorrect, accuracy %, average response time (ms), and longest correct streak. Optionally store best correct count by difficulty in localStorage; no account or backend.

## Visual and technical requirements
- Responsive, accessible, dark-themed standalone HTML file.
- Vanilla HTML/CSS/JS; no dependencies.
- iPhone Safari, Android, desktop browser support.
- Do not add Next button or force manual progression.
- Avoid submitting duplicate answers during the feedback transition.
- Automatically pause if the tab is hidden.
- Link back to `../index.html`.
- Deployable as `games/stroop-challenge.html` on GitHub Pages.

## Acceptance checks
- Selecting the correct ink color scores correct even when the written word differs.
- Incorrect answers score wrong and still auto-advance after 300 ms.
- A single tap cannot register twice.
- Pause hides the answer and freezes time; Resume continues.
- Timed rounds end automatically and show results.
- Practice runs untimed until a new round is started.
