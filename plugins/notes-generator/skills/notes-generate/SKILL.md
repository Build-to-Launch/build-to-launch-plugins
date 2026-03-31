---
name: notes-generate
description: Turn any article into 3–5 ready-to-post Substack notes using a content-type formula system. Each note uses a different angle — diagnostic, story, how-to, contrarian, or observation. Run notes-setup first if NOTES_CONFIG.md doesn't exist.
user-invocable: true
argument-hint: [paste article or provide file path]
---

# Build to Launch: Notes Generate

Turn any article into ready-to-post Substack notes.

## Step 1 — Load config

Check for `NOTES_CONFIG.md` in the project root.
- If missing: tell the user to run `/notes-setup` first, then stop.
- If found: read it. Load tone, style rules, never-do list, and example note.

## Step 2 — Get the article

Ask the user to paste the article text or provide a file path.
Read the full article before doing anything.

## Step 3 — Identify content types

Read the article and identify which content types are present:

| Type | What to look for |
|---|---|
| **diagnostic** | Problem identification — "most people", "the mistake is", "the gap is" |
| **how-to** | Step-by-step process — "here's how", "step 1", framework or workflow |
| **personal story** | First-person narrative — "when I", "I realized", a specific moment |
| **contrarian** | Challenges a belief — "actually", "everyone thinks X but", "wrong" |
| **observation** | Pattern recognition — "I've noticed", "every time", "the pattern is" |
| **wisdom** | Universal principle — "the truth is", "the key to", "what nobody says" |
| **resource** | Tool or method recommendation — "I use", "this changed", specific tool |

Most articles contain 2–4 types. Extract the specific content (problems, steps, stories, principles) for each type found.

## Step 4 — Pick formulas

Match each content type to a note formula:

| Content type | Formula | Structure |
|---|---|---|
| diagnostic | **Parallel repetition** | 3 parallel statements with repeated structure + one closing line |
| how-to | **Bullet list** | Hook + 3–5 numbered steps + one insight at the end |
| how-to | **Technique reveal** | Here's a specific thing I do + why it works + what changes |
| personal story | **Story arc** | Setup → what changed → lesson in one line |
| contrarian | **Expectation reversal** | What people expect + what actually happens + what to do instead |
| observation | **Conditional framework** | If [situation] → [what this means] × 3 + one closing principle |
| wisdom | **Direct statement** | One bold claim + 2–3 supporting specifics + one repeatable line |
| resource | **Before/after** | What I used to do + what I do now + the difference it makes |

Pick the top 3–5 type+formula combinations based on what's richest in the article.

## Step 5 — Generate notes

For each selected combination, write one note following the formula structure.

Apply voice rules from `NOTES_CONFIG.md`:
- Match the 3-word tone exactly
- Follow sentence style preference
- Apply the never-do list — remove anything on it
- Reference the example note for voice calibration if provided

Universal note rules (regardless of config):
- 40–80 words per note
- Payoff first — no setup before the insight
- One idea per note — don't try to say three things
- Last line should be quotable — one line people want to share
- No emojis, no hype words, no vague advice

## Step 6 — Self-assess each note

Score each note 1–10 against:
1. Does the first line stop the scroll?
2. Is the payoff first (no setup)?
3. Is it specific — not generic advice that could apply to anything?
4. Does it create tension — does the reader think "wait, what?"
5. Is it clean — no filler, no hype?
6. Does it have one quotable line?
7. Does it stand alone without needing the article?

If score < 7: revise once and rescore. If still < 7: discard and note why.

## Step 7 — Output

```
Generated [N] notes from "[Article Title]"

──────────────────────────────────────────
Note 1 | [Formula] | Score: X/10
[Note content]

──────────────────────────────────────────
Note 2 | [Formula] | Score: X/10
[Note content]

... (continue for all notes)

──────────────────────────────────────────
Summary
  Total: N notes
  Formulas: [list]
  Ready to post: [N notes scoring 7+]
```

Ask: "Want me to schedule these, or adjust any of them?"
