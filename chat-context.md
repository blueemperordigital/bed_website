# Blue Emperor Digital — Chat Context

Paste this at the start of any new Claude.ai chat for this project.

---

## Project
Boutique digital marketing agency website. Owner: Sherron Gibbs. Location: Homestead, FL.
Files: index.html, about.html, services.html, contact.html, assets/css/styles.css

## Current Phase
Phase 2 — Visual Design & Animation
Hero redesign, colour palette, Georgia font, butterfly animation applied.
Next: Content refinement, Webflow migration, performance pass.

## Brand Colors (priority order)
- Primary: #8CC5C5 (Tiffany Blue) — accents, icons, borders
- Secondary: #C5E2E2 (Light Cyan) — backgrounds, badges
- Accent: #2E9797 (Dark Cyan) — nav, headings
- CTA only: #FF6F61 (Coral) — buttons and highlights only, never overuse
- Body text: #575757 (Davy's Gray)
- Background: #F4FAFA / #E8F5F5 (alt)
- Nav: #2E9797 · Footer: #1A3535 · Headings: #2A4A4A

## Typography
Georgia, serif — all fonts. No Google Fonts.

## Key Decisions
- Coral CTAs only — preserves click urgency
- Background #F4FAFA — tinted white, not pure white
- Butterfly: tiffany blue SVG, Lissajous path, lerp 0.028, scroll drift
- CSS hostable via GitHub + jsDelivr for Webflow
- .claude/settings.json has pre-approved tools (no rm)
- CLAUDE.md in project root for Claude Code instructions
- Every Claude Code task = new branch + PR (feat/ style/ fix/ content/ chore/)

## How to work with me
- Token-efficient responses. Code only, no explanations unless I ask.
- Targeted edits only — no full file rewrites for small changes.
- No preamble, no post-task summaries.
- Confirm scope before starting any large task.
- When we make a new decision, I'll say "update project instructions" — give me
  updated versions of both this file and CLAUDE.md reflecting the change.
- Every prompt updates CLAUDE.md and chat-context.md in same commit if any spec or decision changed