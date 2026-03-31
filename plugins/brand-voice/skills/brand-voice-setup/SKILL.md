---
name: brand-voice-setup
description: Walk the user through defining their brand voice rules — banned words, tone guidelines, opener patterns, and sentence style. Saves rules to BRAND_VOICE.md in their project. Run this once before using brand-voice-check.
user-invocable: true
---

# Build to Launch: Brand Voice Setup

Help the user define their brand voice rules so Claude can enforce them consistently across all their content.

## What to capture

Work through these sections with the user one at a time. Ask, listen, confirm.

### 1. Brand identity (2–3 sentences)
- What do you do / what's your mission?
- Who are you writing for? (be specific — not "entrepreneurs", but what kind)
- What feeling should your content leave readers with?

### 2. Banned words
- Words that sound off-brand, too corporate, too generic, or too buzzword-y
- Prompt: "Are there words you cringe at when you see them in your niche?"
- Add to list. No need for exhaustive — 10–20 strong ones is enough.

### 3. Banned openers and setup phrases
- Phrases you never want to start a sentence or paragraph with
- Prompt: "What opening lines make you immediately distrust a piece of content?"

### 4. Tone in 3 words
- Ask: "Describe your writing tone in exactly 3 words."
- These become the filter: does this sentence match those 3 words?

### 5. Sentence style
- Short and punchy vs. longer and flowing?
- First person or second person dominant?
- Any structural patterns you always use or always avoid?

### 6. What you never do
- Topics, angles, or framings that are off-limits
- Prompt: "What would make a reader think this wasn't written by you?"

## Output

Once you have answers, write them to `BRAND_VOICE.md` in the current project root:

```markdown
# Brand Voice Rules

## Identity
[mission + audience + feeling]

## Banned Words
[comma-separated list]

## Banned Openers
[list]

## Tone
[3 words]

## Sentence Style
[description]

## Never Do
[list]
```

Confirm with the user before writing. Tell them: "You can edit this file any time. Run /brand-voice-check on any piece of content to enforce these rules."
