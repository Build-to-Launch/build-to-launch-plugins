---
name: brand-voice-check
description: Audit any content against the user's brand voice rules defined in BRAND_VOICE.md. Flags violations, suggests fixes, and scores overall brand alignment. Run brand-voice-setup first if BRAND_VOICE.md doesn't exist.
user-invocable: true
argument-hint: [paste content or provide file path]
---

# Build to Launch: Brand Voice Check

Audit content against the user's brand voice rules and return a clear, actionable report.

## Workflow

1. Check if `BRAND_VOICE.md` exists in the project root
   - If not: tell the user to run `/brand-voice-setup` first, then stop
   - If yes: read it fully before proceeding

2. Ask the user to paste the content to check (or accept a file path)

3. Read the full content before flagging anything

4. Audit against each section of `BRAND_VOICE.md`:
   - **Banned words**: flag every occurrence, line number + word
   - **Banned openers**: flag any paragraph or sentence starting with a banned pattern
   - **Tone**: read the full piece — does it match the 3-word tone? Note where it drifts
   - **Sentence style**: flag structural patterns that break the defined style
   - **Never do**: flag any topics, angles, or framings on the off-limits list

5. Score overall brand alignment: Strong / Needs work / Off-brand
   - Strong = 0–2 minor violations
   - Needs work = 3–6 violations or 1 tone drift
   - Off-brand = structural mismatch or multiple tone breaks

## Output format

```
## Brand Voice Check

**Overall: [Strong / Needs work / Off-brand]**

### Violations
- Line X: "[quoted text]" — banned word: [word]. Suggest: [alternative]
- Para 2: Opens with "[opener]" — banned opener. Suggest: [rewrite]

### Tone drift
[Note where the piece loses the 3-word tone and what shifted]

### What's working
[1–2 things that nail the brand voice — always include this]

### Suggested rewrites
[For the top 2–3 violations, show the before/after]
```

Always end with what's working — the goal is calibration, not criticism.
