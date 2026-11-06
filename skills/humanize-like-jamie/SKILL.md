---
name: humanize-like-jamie
description: |
  Write or rewrite text in Jamie's voice: the writing style of Jamie Eduardo
  C. Rosal, Philippine engineering researcher. Humanize AI-sounding text into
  that voice, or draft new text from a brief in it, without changing any
  facts. Use when the user asks to write like Jamie, humanize like Jamie, or
  match Jamie's writing style.
license: MIT
metadata:
  version: "3.2.0"
---

# Write like Jamie

Write and rewrite text in Jamie's voice. Keep what the text says. Do not
make anything up.

Jamie is Jamie Eduardo C. Rosal, a Filipino engineering researcher. The
voice lives in two files that you must read before writing:

1. `STYLE.md` in this skill folder — the distilled profile.
2. `samples/sample1.md`, `samples/sample2.md`, `samples/sample3.md` — full
   papers (2018, 2022, 2026) in the voice. They are the ground truth. If the
   profile disagrees with the samples, follow the samples.

## How to work

1. **Read the voice first.** Load `STYLE.md`, then at least one full sample.
   For an academic task read all three and lean on the newest, `sample3.md`.
2. **Decide the mode.** If the user pasted text, rewrite it. If the user gave
   a topic, outline, or brief, draft new text. Say which mode you are in.
3. **Rewrite mode.** Remove AI writing tells first: not-X-but-Y contrasts,
   one-line closers, staged openers, forced triads, inflated claims, stock AI
   words, bold labels. If the `humanizer` skill is installed, use its full
   pattern list for this pass; otherwise the list above covers the
   strongest tells. Then re-voice the clean result as Jamie, following
   `STYLE.md`. Facts, names, numbers, dates, quotes, and citations must stay
   exactly as the source gives them.
4. **Draft mode.** Build the text in Jamie's structure. Academic work uses
   the IEEE paper skeleton from `STYLE.md`. Fill every section you were given
   material for; leave a clear placeholder and tell the user rather than
   inventing content for a section you lack data for.
5. **Check.** Read the result once against `STYLE.md`'s signature moves and
   word habits. Ask what still sounds generic, then fix it. The result must
   sound like the samples, not like a chatbot imitating an academic.

## Faithfulness dial

Default is clean Jamie: his sentence rhythm, passive voice, connectors,
framing moves, number style, and signature phrases, with grammar kept
correct. If the user asks for fuller fidelity ("quirks on", "write it exactly
like him"), also reproduce his grammar slips as described in `STYLE.md`.
Never let a quirk change a number, date, name, or technical claim.

## What to return

- **Pasted text.** Return the rewrite, a short list of what you changed for
  the voice, and anything you left untouched because it was already in
  Jamie's voice.
- **File mode.** When the user names a file, change prose only. Keep code,
  data, tables, YAML metadata, math, and link targets unchanged, then give
  a short summary.
- **Embedded mode.** When another task uses this skill (commit message,
  cover letter, document), return only the final text.
