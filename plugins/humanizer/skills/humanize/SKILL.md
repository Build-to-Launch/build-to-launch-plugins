---
name: humanize
description: Remove AI-ish phrasing from any content — blog posts, emails, captions, notes — while preserving the author's voice and meaning. Use when the user wants to clean up AI-generated or AI-sounding text.
user-invocable: true
argument-hint: [paste content or describe what to humanize]
---

# Build to Launch: Humanizer

Remove AI-generated patterns from any text while keeping the author's voice intact.

## What this removes

**Banned AI vocabulary** — never use these words:
delve, embark, enlightening, shed light, craft/crafting, realm, game-changer, unlock, discover, skyrocket, revolutionize, disruptive, utilize/utilizing, dive deep, tapestry, illuminate, unveil, pivotal, intricate, hence, harness, groundbreaking, ever-evolving

**Banned setup phrases** — cut completely, go straight to the content:
"Here's what...", "Here's how...", "Here's why...", "Here's the thing...", "The thing is...", "What I discovered was...", "Let me tell you..."

**Banned filler language:**
"In conclusion", "Moreover", "Furthermore", "It's worth noting that", "It's important to understand that"

**Formulaic contrasts** — never use:
"It's not X, it's Y", "It wasn't just X — it was Y", "Not just X, but Y"

## What this preserves

- The author's tone, perspective, and voice
- All factual content and structure
- Technical terms that are genuinely needed
- Short punchy sentences (these are good — keep them)

## Workflow

1. Ask the user to paste the content to humanize (or they may paste it directly)
2. Read the full text before making changes
3. Apply all removals above — replace, rewrite, or cut as needed
4. Check intensifiers: "actually", "truly", "genuinely", "just", "really" — read with and without. Cut if removing loses nothing. Keep if it adds real contrast.
5. Check em-dashes: maximum 2–3 per piece. For every em-dash, try a period first, then comma, then colon, then restructure. Only keep for genuine dramatic punch.
6. Return the cleaned version with a brief note on what changed

## Output format

Return the humanized text in full, followed by:
- A one-line summary of the main patterns removed
- Any sentences that needed significant restructuring (so the author can review intent)

## Example

User: "Let's delve into how you can harness the power of AI to craft compelling content that truly revolutionizes your workflow."

→ "Here's how AI can improve your content workflow." ← still setup-y

→ Better: "AI can cut your content workflow in half. Here's how."

→ Best: Start directly with the first real point — skip the setup entirely.
