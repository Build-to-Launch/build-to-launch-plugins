---
name: research-setup
description: First-time setup for the research-digest plugin. Defines what topics to track, what content already exists, and where to save digests. Run this once before using research-digest.
user-invocable: true
---

# Build to Launch: Research Setup

Configure the research digest for your niche. Run this once — takes 5 minutes.

## What to capture

Work through each section with the user. Ask, confirm, then write the config files.

### 1. Topics to track

Ask: "What topics do you cover? List 5–10 — be specific. Not 'AI' but 'Claude Code', 'vibe coding', 'building with LLMs'."

Each topic becomes a tracked search term run weekly against Reddit, Hacker News, and the web.

Good topics:
- Specific tools, frameworks, platforms ("Cursor", "Supabase", "n8n")
- Pain points your audience has ("automating client work", "building without code")
- Adjacent topics that feed your niche ("prompt engineering", "AI agents")

### 2. Existing content (for deduplication)

Ask: "Do you have a list of articles or posts you've already published? Paste titles or a file path."

This prevents the digest from surfacing topics you've already covered.

If none yet: skip — the digest will surface all opportunities without filtering.

### 3. Output folder

Ask: "Where should weekly digests be saved?" Default: `./research-digests/`

### 4. Niche summary (1 sentence)

Ask: "Describe your audience in one sentence — who they are and what they're trying to do."

This is used as context when scoring whether a topic is relevant to your niche.

## Output

Write two files:

**`RESEARCH_CONFIG.md`** in the project root:
```markdown
# Research Config

## Niche
[one-sentence audience description]

## Topics
- [topic 1]
- [topic 2]
- [topic 3]
...

## Existing Content
- [title 1]
- [title 2]
...

## Output Folder
[path — default: ./research-digests/]
```

**`research-digests/.gitkeep`** to create the output folder.

Confirm before writing. Tell the user: "Run /research-digest any time to get this week's top content opportunities."
