---
name: btl-unlock
description: Activate a Build to Launch premium plugin using your Substack subscriber email. Premium plugins are included with a paid Build to Launch subscription — no separate purchase needed.
user-invocable: true
argument-hint: [your subscriber email]
---

# Build to Launch: Activate Premium Plugin

Premium plugins are included with a paid Build to Launch subscription.

## Workflow

1. Ask the user for their Substack subscriber email (the one they use at buildtolaunch.substack.com)

2. Call `activate_plugin` with their email and the plugin_id:
   - `newsletter-engine` — full newsletter production system
   - `ai-builder-toolkit` — content system for AI builders

3. If valid: confirm which skills are now available
   - `newsletter-engine`: `/research-digest` `/article-draft` `/notes-generate` `/seo-check` `/publish-substack`
   - `ai-builder-toolkit`: `/weekly-plan` `/build-in-public` `/content-pillars` `/distribute`

4. If not found: direct them to subscribe at buildtolaunch.substack.com

## Notes

- Activation is cached on this machine — email only needed once
- To check what's active: call `check_plugin_status`
- To deactivate (e.g. moving machines): call `deactivate_plugin`
