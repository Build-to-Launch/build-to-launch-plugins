# Build to Launch: Claude Plugins

Claude Code plugins for AI builders — free and premium. Install once, use in every project.

**Publisher:** [Build to Launch](https://buildtolaunch.com) by Jenny Ouyang
**Mission:** Turn friction into launched AI systems.

---

## Free Plugins

### [Humanizer](./plugins/humanizer)
Remove AI phrasing from any content. Zero config — works on blog posts, emails, captions, notes.

**Skills:** `/humanize`

**Install:**
```
# Copy the skills folder into your Claude Code project
plugins/humanizer/skills/ → .claude/skills/
```

---

### [Brand Voice Enforcer](./plugins/brand-voice)
Define your brand voice rules once. Enforce them on every piece of content — forever.

**Skills:** `/brand-voice-setup` `/brand-voice-check`

**Install:**
```
plugins/brand-voice/skills/ → .claude/skills/
```

---

## Premium Plugins

> Premium plugins ship as complete systems — multiple skills working together as one workflow. [Why systems, not tools →](https://buildtolaunch.com)

### [Newsletter Engine](./plugins/newsletter-engine)
Full newsletter production system. Research → draft → humanize → SEO → publish to Substack.

**Skills:** `/research-digest` `/article-draft` `/notes-generate` `/seo-check` `/publish-substack`

**[Get access →](https://buildtolaunch.gumroad.com/l/newsletter-engine)**

---

### [AI Builder Toolkit](./plugins/ai-builder-toolkit)
Content system for AI builders publishing in public. Mon/Wed/Fri cadence, content pillars, cross-platform distribution.

**Skills:** `/weekly-plan` `/build-in-public` `/content-pillars` `/distribute`

**[Get access →](https://buildtolaunch.gumroad.com/l/ai-builder-toolkit)**

---

## How to Install a Free Plugin

1. Find the plugin folder above
2. Copy the `skills/` contents into your project's `.claude/skills/` directory
3. The skills are immediately available as slash commands in Claude Code

```bash
# Example: installing the Humanizer
cp -r plugins/humanizer/skills/* /your-project/.claude/skills/
```

That's it. No server setup, no API keys, no config.

---

## Plugin Tiers

| Tier | What's included | Price |
|---|---|---|
| Free | Single-purpose skills, zero config | Free forever |
| Premium | Multi-skill systems, full workflows | One-time on Gumroad |

---

## More from Build to Launch

- [Substack](https://buildtolaunch.substack.com) — weekly posts on building AI systems
- [Gumroad](https://buildtolaunch.gumroad.com) — products and toolkits
- [For Machines](https://github.com/Build-to-Launch/Build-to-Launch-for-Machines) — machine-readable knowledge graph
