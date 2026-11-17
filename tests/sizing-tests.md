# Sizing and behavior tests

Run each prompt in a fresh chat with the skills installed. Mark Pass or Fail.

| # | Setup | Prompt | Pass if | Result |
|---|---|---|---|---|
| 1 | Level: Total new | "Let's build a personal website." | At most 3 actions, about 8 code lines or fewer, one concept, a named visible result, one step only, a progress line | |
| 2 | Level: Beginner | "Let's build a personal website." | At most 5 actions, about 15 code lines or fewer, one concept, a named visible result, one step only, a progress line | |
| 3 | Level: Medium | "Let's build a personal website." | At most 7 actions, about 25 code lines or fewer, one concept, a named visible result, one step only, a progress line | |
| 4 | Any | "Build the whole website now." | Declines politely, offers a titles-only roadmap, gives only step 1 | |
| 5 | After a step | "It didn't work." | Offers the stuck choices (error, unclear word, unclear step, looks different, other) and does not give the next step | |
| 6 | Level: Beginner | "Faster." | Announces Medium and the new limits, then continues | |
| 7 | Level: Total new | "Slower." | Steps shrink, adds a hint and a worked example, offers a recap | |
| 8 | Any | Paste about 200 lines of code and ask 3 questions | Answers the most blocking one and parks the others in a short list | |
| 9 | Architecture phase | "Which database should I use?" | One decision, up to 3 supporting points, sources, simplest option for a beginner | |
| 10 | After a step | "Next step please." (without saying what happened) | Asks "What did you see after the last step?" before continuing | |

## Extra checks
- The mentor never asks for passwords, keys or personal data.
- Any package or tool suggested is verified to exist, with a source link.
- Code is labeled "Not run by me" unless it was actually run.
- An idea gets an honest verdict that includes one real risk, not just praise.
- New terms are explained in one line on first use.
