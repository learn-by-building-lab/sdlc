# SDLC Mentor

A set of AI skills that mentor a beginner through building an app or website, one small step at a time. The mentor first tunes your idea, then walks the software development lifecycle with a role for each phase (Idea Coach, Business Analyst, Project Manager, Architect, Designer, Scrum Master, Developer, QA Tester, DevOps and Reviewer).

**Status:** early draft, not yet tested with real learners.

## Why
Research on AI and learning suggests that AI without guardrails can help students finish tasks while hurting what they learn, and that AI tutors often go unused. This project tries a different approach: small steps, the learner does the work, and every claim is checked against sources.

## Skills
| Skill | What it does |
|---|---|
| `sdlc-mentor` | The main mentor: idea tuning, roles, phases, step format, guardrails |
| `sdlc-mentor-help` | Handles "I'm stuck" with a short multiple-choice diagnosis |
| `sdlc-mentor-level` | Changes the step size when the learner says faster or slower |
| `sdlc-mentor-intro` | Short introduction to what the mentor can do |

## How it works
- **Levels:** Total new, Beginner or Medium, picked by the learner and confirmed with two quick questions.
- **Step limits:** up to 3, 5 or 7 actions and about 8, 15 or 25 lines of code per step.
- **Steps:** 10 to 20 minutes, one concept, and a visible result you can check.
- **Progress:** a titles-only roadmap plus a progress line on every reply.
- **Guardrails:** one step per reply, short by default, verify claims with sources, no invented packages, label untested code, challenge ideas honestly, never ask for secrets.

## Install
Each folder in `skills/` is one skill containing a `SKILL.md` file. Add the folders to your Claude setup (for example, by zipping a skill folder and uploading it in your skills settings, or by placing it in your skills directory when using Claude Code). Check the current Claude documentation for the exact steps.

## Test it
Use the prompts in [`tests/sizing-tests.md`](tests/sizing-tests.md) and record pass or fail. Please open an issue with any prompt that makes the mentor break its own rules.

## Known limits
- Skills are instructions, not enforced rules, so a model can still drift in long conversations.
- Fact-checking is best effort. Double-check anything important.
- Helper-agent model routing only works in setups that provide a helper-agent tool.

## Contributing
Issues and suggestions are welcome, especially failing test prompts and ideas for making steps clearer for beginners.

## License
Not chosen yet. Add a `LICENSE` file before publishing (common choices for open source are MIT and Apache 2.0).
