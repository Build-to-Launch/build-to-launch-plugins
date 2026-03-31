---
name: build-in-public-setup
description: First-time setup for the build-in-public plugin. Defines what you're building, who you're building for, and what format your build updates should take. Run once before using build-in-public.
user-invocable: true
---

# Build to Launch: Build in Public Setup

Define your builder profile so every update sounds grounded and specific — not generic.

## What to capture

### 1. What you're building

Ask: "What are you building right now? Be specific — not 'an app' but what it does, who it's for, and where it's at."

Examples:
- "A Claude Code plugin marketplace for newsletter writers — just launched the first two plugins"
- "A SaaS tool that auto-generates client reports from Notion — in private beta with 12 users"
- "A Substack newsletter about AI for non-technical founders — 3 months in, 400 subscribers"

### 2. Who you're building for

Ask: "Who's your audience — the person you're building for AND the person reading your build updates?"

Often the same, sometimes different. A founder building a B2B tool might be writing for other founders, not customers.

### 3. What you share in updates

Ask: "What kind of build moments do you want to document? Check all that apply:"
- Shipped something new
- Hit a milestone (subscribers, revenue, users)
- Made a decision (pivoted, cut a feature, changed direction)
- Learned something the hard way
- Got stuck and figured it out
- Had a conversation that changed my thinking

### 4. Your publishing channel

Ask: "Where do you post build updates?" (Substack, X/Twitter, LinkedIn, all of them)

This affects length and format of the output.

### 5. One example update you liked (optional)

Ask: "Paste a build update you've written that felt right — or one you admire from someone else."

## Output

Write `BUILD_CONFIG.md` in the project root:

```markdown
# Build in Public Config

## What I'm Building
[description]

## Who I'm Building For
[audience]

## What I Share
[checked items]

## Publishing Channel
[channel(s)]

## Example Update
[paste or leave blank]
```

Confirm before writing. Tell the user: "Run /build-in-public any time you have a build moment to share — ship, lesson, milestone, or decision."
