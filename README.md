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
Each folder in `skills/` is one skill containing a `SKILL.md` file. Install all four, since the main mentor hands off to the other three.

### Claude Code, quickest way (plugin)
Run these as two separate commands inside Claude Code:
```
/plugin marketplace add SuprajyotsnaDasari-lab/sdlc
/plugin install sdlc-mentor@sdlc-mentor
```
Then start a new session. The skills appear as `/sdlc-mentor:sdlc-mentor`, `/sdlc-mentor:sdlc-mentor-help` and so on.

### Claude Code, manual copy
1. Download the project:
   ```bash
   git clone https://github.com/SuprajyotsnaDasari-lab/sdlc.git
   cd sdlc
   ```
2. Copy the skills into your personal skills folder (they work in every project):
   ```bash
   mkdir -p ~/.claude/skills
   cp -R skills/* ~/.claude/skills/
   ```
   To use them in one project only, copy them into that project's `.claude/skills/` folder instead.
3. Start a new Claude Code session (existing sessions don't see new skills).
4. Check it worked: type `/` and look for `sdlc-mentor`, or ask "what skills do you have?".

### Codex (CLI and desktop app)
Plugin install (same two commands for the desktop app, then restart the app):
```bash
codex plugin marketplace add SuprajyotsnaDasari-lab/sdlc
codex plugin add sdlc-mentor@sdlc-mentor
```
Or copy the skills by hand (Codex reads `SKILL.md` files from `~/.agents/skills`):
```bash
mkdir -p ~/.agents/skills
cp -R skills/* ~/.agents/skills/
```
Start a new thread. In the CLI, type `$` or `/skills` to pick a skill. In the desktop app, open Skills in the sidebar to see them.

### ChatGPT desktop app
Standalone skills are supported in the ChatGPT desktop app. Add the four skill folders using the app's skills settings (the exact menu may change, so check OpenAI's current docs), then type `@` and pick `sdlc-mentor` to start. The web and mobile ChatGPT apps only run skills that come inside a plugin.

> The Codex and ChatGPT steps follow OpenAI's skills docs and are untested here.

### Claude.ai (web or desktop chat)
1. Download the project from GitHub (Code > Download ZIP) and unzip it.
2. Zip each skill folder on its own, so `SKILL.md` sits directly inside the folder (for example `sdlc-mentor.zip`).
3. Go to Settings > Capabilities > Skills, choose Upload skill, and upload each of the four zips.
4. Turn each skill on. Menu names can change, so check the current Claude documentation if you don't see them.

### Use it
Start a new chat and say something like "I want to build a website" or "/sdlc-mentor". The mentor will ask about your idea and your level first.

### Update or remove
- Update: `git pull`, then copy the folders over again.
- Remove: delete the `sdlc-mentor*` folders from `~/.claude/skills/`.

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
