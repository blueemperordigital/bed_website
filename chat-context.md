# Blue Emperor Digital — Chat Context

Paste this at the start of any new Claude.ai chat for this project.

---

## Project
Boutique digital marketing agency website. Owner: Sherron Gibbs. Location: Homestead, FL.
Project root: `C:\Users\sherr\Desktop\Blue Emperor Digital\Blue Emperor Digital\Website\bed_website`
Files: index.html, about.html, services.html, contact.html, assets/css/styles.css

## Current Phase
Phase 2 — Webflow Build (Hybrid approach: Webflow Designer for layout, inject Claude-generated CSS/JS for custom touches)

## Build Approach
Hybrid — Webflow Designer handles layout, navigation, responsiveness, CMS, hosting, forms, SEO meta. Claude generates CSS for design system and JS for custom animations (butterfly), pasted into Webflow Project Settings → Custom Code.

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

## Services (9 confirmed per blueprint)
1. Web Design & Development
2. SEO & Local SEO
3. Social Media Management
4. PPC & Paid Advertising
5. Content Marketing
6. Email Marketing
7. Analytics & Reporting
8. AI-Driven Marketing
9. Case Studies/Results

## Key Decisions
- Coral CTAs only — preserves click urgency
- Background #F4FAFA — tinted white, not pure white
- Butterfly: tiffany blue SVG, Lissajous path, lerp 0.028, scroll drift
- CSS hostable via GitHub + jsDelivr for Webflow
- .claude/settings.json has pre-approved tools (no rm)
- CLAUDE.md in project root for Claude Code instructions
- Every Claude Code task = new branch + PR (feat/ style/ fix/ content/ chore/)
- PRs created automatically via gh pr create — GitHub CLI installed and authenticated
- gh CLI PATH issue resolved — Claude Code finds gh correctly. No reinstall needed if gh pr create works.
- Building from scratch in Webflow Designer (not template) for learning + control
- 9 services confirmed per blueprint, expand from current 6
- Phase 1 partially complete: Operating Agreement, bank account, domain, Workspace email, contracts done. Pending: LLC filing, EIN, Registered Agent, Wave Accounting, E&O insurance. Sherron handling separately.
- Existing coded site (HTML/CSS) preserved as reference + backup, not used as live site

## How to work with me
- Token-efficient responses. Code only, no explanations unless I ask.
- Targeted edits only — no full file rewrites for small changes.
- No preamble, no post-task summaries.
- Confirm scope before starting any large task.
- When we make a new decision, I'll say "update project instructions" — give me
  updated versions of both this file and CLAUDE.md reflecting the change.
- Every prompt updates CLAUDE.md and chat-context.md in same commit if any spec or decision changed

## Important Clarifications
- chat-context.md is the source for these project instructions — update project 
  instructions manually after each merge that changes chat-context.md
- CLAUDE.md is for Claude Code (CLI) only — not relevant to chat context
- This is a Claude.ai Project — instructions persist across chats automatically, 
  no need to paste context manually