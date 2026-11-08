# Six Thinking Hats Facilitator

A skill that turns the model into a strict **Blue Hat** facilitator for Edward de Bono's Six Thinking Hats method.

Unlike skills that have the model analyse a problem from all six perspectives itself, this one keeps the model out of the content entirely. It manages the process (focus, sequence, time boxes, summaries), and **you** supply all the facts, feelings, risks, benefits and ideas. The model won't add its own, not even as hints.

## What a session looks like

1. **Setup (Blue).** You state the focus question in one sentence. The model proposes a hat sequence that fits the situation (general decision, evaluating a proposal, solving a problem, finding ideas, choosing between options, emotionally loaded situation, or a quick 10-minute check) and explains why that order fits.
2. **One hat at a time.** For each hat the model gives a one-line intro and a time box, then asks one or two neutral, open questions. You answer in as many messages as you like. If you drift into another hat, the point gets parked for later.
3. **Summaries in your own words.** When you say *next*, the model summarizes only what you said under that hat, with nothing added or reinterpreted.
4. **Final roadmap (Blue).** A consolidated summary per hat, then your decision, next steps (owner and date), open questions, and a revisit trigger.

## Commands during a session

| Command | Effect |
|---|---|
| `next` (also `done`, `move on`, `naprej`, `naslednji`, `dalje`) | Summarize the current hat and move to the next one |
| `back` | Return to the previous hat and add to it |
| `skip` | Skip the current hat (noted in the final synthesis) |
| `change sequence` | Re-plan the remaining hats |
| `stop` | Jump straight to the final synthesis |

## Usage

Invoke the skill with an optional topic, for example in Claude Code:

```
/six-hats-facilitator Should we move our team to a four-day week?
```

Or just ask for a Six Thinking Hats session in conversation. The session runs in the language you write in, Slovenian included.

## Installation

See the [repository README](../../README.md#installation).
