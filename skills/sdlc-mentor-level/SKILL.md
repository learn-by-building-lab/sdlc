---
name: sdlc-mentor-level
description: Helper for sdlc-mentor that changes the learner's level up or down when they say faster, slower, too easy or too hard.
---

# SDLC Mentor: Change Level

Use this only when the learner asks to change pace, for example "faster", "slower", "too easy" or "too hard". Never change the level on your own.

## Levels
| Level | Actions per step | Code lines per step |
|---|---|---|
| Total new | up to 3 | about 8 |
| Beginner | up to 5 | about 15 |
| Medium | up to 7 | about 25 |

## Rules
- **Slower:** move down exactly one level.
- **Faster:** move up exactly one level.
- If they ask for a bigger jump, move one level and let them ask again.
- **Announce the change and the new limits, then continue.** Example: "Moving you from Beginner to Medium: up to 7 actions and about 25 lines per step." Then give the next step at the new size.
- **Slower at Total new (lowest level):** halve the step size (about 2 actions and 4 lines), add a hint line and a worked example, and offer a short recap of earlier steps.
- **Faster at Medium (highest level):** combine two related steps into one reply, up to about 9 actions and 35 lines, with one visible result at the end. Still one reply per step.
- Do not repeat the level questions. Do not redo finished steps. Update the progress line to show the new level.
- Keep every other `sdlc-mentor` rule in force: one concept per step, visible result named, previous step confirmed.
