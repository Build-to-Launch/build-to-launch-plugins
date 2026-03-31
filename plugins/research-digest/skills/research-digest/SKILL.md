---
name: research-digest
description: Run the weekly content research digest. Searches Reddit, Hacker News, and the web for each tracked topic, scores content opportunities, and outputs a ranked list of what to write next. Run research-setup first if RESEARCH_CONFIG.md doesn't exist.
user-invocable: true
---

# Build to Launch: Research Digest

Run weekly content research and produce a ranked opportunity digest.

## Step 1 — Load config

Check for `RESEARCH_CONFIG.md` in the project root.
- If missing: tell the user to run `/research-setup` first, then stop.
- If found: read it. Extract topics, niche summary, existing content list, and output folder.

## Step 2 — Research each topic

For each topic in the config, search:

**Reddit** — use Perplexity with `source_focus: "social"`:
- Query: `site:reddit.com "[topic]"` — last 30 days
- Look for: threads with 10+ comments, unresolved questions, repeated complaints

**Hacker News** — use Perplexity with `source_focus: "web"`:
- Query: `site:news.ycombinator.com "[topic]"`
- Look for: Show HN posts, Ask HN questions, comment threads with strong engagement

**Web** — use Perplexity with `source_focus: "web"`:
- Query: `"[topic]" tutorial OR guide OR how to — last month`
- Look for: gaps where the existing content is outdated, thin, or missing a key angle

Group related topics into clusters before searching — don't run 10 identical searches.

## Step 3 — Score each opportunity

For each unique pain point or topic surfaced, score out of 10:

| Signal | Points | How to measure |
|---|---|---|
| Community engagement | 3 pts | 50+ upvotes or 20+ comments = 3pts. 10–49 = 2pts. Under 10 = 1pt. |
| Search demand | 3 pts | High-volume query with thin results = 3pts. Moderate = 2pts. Low = 1pt. |
| Content gap | 4 pts | No satisfying answer exists (+2), not in your existing content (+2) |

Pick the **top 3** opportunities.

## Step 4 — Filter duplicates

Before finalizing, check each top-3 against the existing content list from `RESEARCH_CONFIG.md`.
If a topic is clearly already covered (same angle, same question), drop it and pull in #4.

## Step 5 — Write the digest

Save to the output folder defined in `RESEARCH_CONFIG.md`. Filename: `YYYY-MM-DD.md`.
If a file for today already exists, skip — digest already ran today.

```markdown
# Research Digest — YYYY-MM-DD

## Top Opportunities

### 1. [Topic] — Score: X/10
**Source:** Reddit r/[subreddit] (N upvotes) / HN / Web
**Signal:** [one sentence — what people are asking or complaining about]
**Why now:** [one line — timing, trend, or recency]
**Suggested angle:** [Free article / Short post / Deep guide]
**Suggested title:** [draft title]

### 2. [Topic] — Score: X/10
...

### 3. [Topic] — Score: X/10
...

## Filtered Out (already covered)
- [topic] — matches "[existing content title]"

## Watchlist Suggestions
**Consider adding:** [new topic] — appeared in N threads this week, not currently tracked
**Consider removing:** [existing topic] — fully covered, no new angles appearing

## Research run
- Topics searched: N
- Sources: Reddit, Hacker News, Perplexity web
- Date range: last 30 days
```

## Step 6 — Summary to user

After writing the file, show the top 3 in chat:

```
Research Digest — [date]

1. [Topic] — Score: X/10
   "[Suggested title]"

2. [Topic] — Score: X/10
   "[Suggested title]"

3. [Topic] — Score: X/10
   "[Suggested title]"

Full digest saved to [output folder]/YYYY-MM-DD.md
```

Ask: "Want me to start drafting any of these?"
