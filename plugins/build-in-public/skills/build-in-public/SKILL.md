---
name: build-in-public
description: Turn a build update into a ready-to-post piece. Tell Claude what happened — shipped, learned, decided, hit a milestone — and get a post that sounds like you, not a press release.
user-invocable: true
argument-hint: [describe what happened — shipped, learned, hit a milestone, made a decision]
---

# Build to Launch: Build in Public

Turn a build moment into a post worth sharing.

## Step 1 — Load config

Check for `BUILD_CONFIG.md` in the project root.
- If missing: tell the user to run `/build-in-public-setup` first, then stop.
- If found: read it. Load what they're building, audience, preferred update types, and publishing channel.

## Step 2 — Get the build moment

Ask the user: "What happened? Tell me in a few sentences — what you shipped, learned, decided, or hit."

Don't lead with format questions. Just get the raw story first.

If they give you a one-liner, ask one follow-up: "What was the specific thing that made this worth sharing?"

## Step 3 — Identify the moment type

Classify what they shared:

| Type | Signals | Core question |
|---|---|---|
| **Shipped** | New feature, product, post, tool | What does it do and why did you build it? |
| **Milestone** | Numbers, subscribers, revenue, users | What got you here — one specific decision? |
| **Decision** | Pivot, cut, changed direction | What were the two options and why did you pick this one? |
| **Lesson** | Made a mistake, figured something out | What did you think before vs. what you know now? |
| **Stuck + solved** | Hit a wall, found a way through | What was the wall and what moved it? |
| **Conversation** | Feedback, user call, comment that changed thinking | What changed and why did it land? |

## Step 4 — Pick a structure

Match the moment type to a structure:

**Shipped:**
> What it is (1 sentence) → Why I built it (1 sentence) → What surprised me building it → Where to get it

**Milestone:**
> The number → The one thing that moved it → What I got wrong before → What's next

**Decision:**
> The choice I faced → What I almost did → Why I went the other way → What I'm watching for

**Lesson:**
> What I thought → What actually happened → The specific thing that changed my mind → One line they can apply

**Stuck + solved:**
> What blocked me → How long I was stuck → What broke it loose → Why this matters beyond my situation

**Conversation:**
> Who I talked to → What they said → What it changed → One question it left me with

## Step 5 — Write the post

Write one version optimized for the primary publishing channel in `BUILD_CONFIG.md`.

**Substack / long-form:** 150–300 words. Room for one extra detail. End with a question or what's next.

**X/Twitter:** 2–4 short paragraphs. Under 280 characters per block. Hook line first.

**LinkedIn:** 150–200 words. First line is the hook. Last line is a question or invitation.

Voice rules:
- Match the tone from `BUILD_CONFIG.md` example update (if provided)
- Specific over vague — real numbers, real names, real moments
- No corporate language ("excited to announce", "thrilled to share", "proud to")
- No fake humility ("just a small thing but...")
- First person throughout
- The last line should be something a reader would remember

## Step 6 — Output

Show the post ready to copy, then ask:

"Want me to adjust the length, add a hook variation, or turn this into a Substack note too?"
