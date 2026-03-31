---
name: notes-setup
description: First-time setup for the notes-generator plugin. Defines your Substack note voice, tone, and style rules so generated notes sound like you. Run once before using notes-generate.
user-invocable: true
---

# Build to Launch: Notes Setup

Define your note voice so every generated note sounds like you wrote it — not like AI wrote it.

## What to capture

### 1. Tone in 3 words

Ask: "Describe how your best notes feel in exactly 3 words."

Examples: "direct, provocative, grounded" / "warm, practical, honest" / "bold, technical, dry"

### 2. Sentence style

Ask: "Short and punchy, or longer and flowing? First person or second person?"

Notes that perform well are usually short (40–80 words), first person, one idea per note.

### 3. What you never do in notes

Ask: "What makes a note feel off-brand for you? What would make you cringe?"

Examples: emojis, motivational-poster phrases, vague advice, hype language, self-promotion.

### 4. One example note you love (optional)

Ask: "Paste one note you've written that felt right, or one from someone else whose style you admire."

This becomes the reference point for voice calibration.

### 5. Your Substack URL (optional)

For adding source links to generated notes.

## Output

Write `NOTES_CONFIG.md` in the project root:

```markdown
# Notes Config

## Tone
[3 words]

## Sentence Style
[description]

## Never Do
[list]

## Example Note
[paste or leave blank]

## Substack URL
[URL or leave blank]
```

Confirm before writing. Tell the user: "Run /notes-generate and paste any article to get 3–5 ready-to-post notes."
