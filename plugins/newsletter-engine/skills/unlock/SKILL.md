---
name: btl-unlock
description: Activate a Build to Launch premium plugin using your Gumroad license key. Run this once per machine after purchasing. Use when the user wants to unlock newsletter-engine or ai-builder-toolkit.
user-invocable: true
argument-hint: [plugin-id] [license-key]
---

# Build to Launch: Unlock Premium Plugin

Activate your premium plugin with your Gumroad license key.

## Workflow

1. Ask the user which plugin they want to unlock if not specified:
   - `newsletter-engine`
   - `ai-builder-toolkit`

2. Ask for their license key — found in their Gumroad receipt email, or at gumroad.com/library

3. Call `validate_license` with the plugin_id and license_key

4. If valid: confirm activation and show which skills are now available
   - `newsletter-engine` unlocks: `/research-digest` `/article-draft` `/notes-generate` `/seo-check` `/publish-substack`
   - `ai-builder-toolkit` unlocks: `/weekly-plan` `/build-in-public` `/content-pillars` `/distribute`

5. If invalid: show the purchase link and what the plugin includes

## Check status

To see which plugins are already activated on this machine, call `check_license_status`.

## Notes

- License is cached locally — you only need to enter it once per machine
- To move your license to a new machine, call `revoke_license` on the old machine first
- Each Gumroad license supports use on up to 2 machines
