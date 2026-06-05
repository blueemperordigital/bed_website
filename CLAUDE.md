# Blue Emperor Digital LLC — Project Instructions

Owner: Sherron Gibbs · Location: Homestead, FL · Serving clients locally & nationally

---

## Current Phase
**Phase 2 — Visual Design & Animation**
Hero redesign, colour palette, Georgia font, butterfly animation, and visual polish applied.
Next: Content refinement, Webflow migration, performance pass.

---

## Build Log
- 2025 | `main` | Initial site built — index, about, services, contact + styles.css
- 2025 | `style/design-system` | Full CSS design system generated (variables, components, animations)
- 2025-06-05 | `style/visual-overhaul` | Georgia font, tiffany-tinted bg, colour hierarchy, butterfly animation, visual polish
- 2026-06-05 | `chore/project-instructions-update` | Added chat-context.md, updated CLAUDE.md with Current Phase, Build Log, Git & PR Workflow, PR format
- 2026-06-05 | `chore/standardise-instruction-updates` | Standardised instruction update process across CLAUDE.md and chat-context.md
- 2026-06-05 | `chore/gh-cli-pr-automation` | Automated PR creation via GitHub CLI, updated settings.json and project instructions

---

## Git & PR Workflow
Every task must follow this flow — no exceptions:

1. **Branch** — create a new branch before making any changes:
   - `feat/` — new functionality
   - `style/` — visual/CSS only
   - `fix/` — bug fixes
   - `content/` — copy or structural changes
   - `chore/` — config, tooling, maintenance
   - Use kebab-case, be specific: `style/butterfly-animation` not `style/update`

2. **Commit** — one focused commit per logical change. Message format:
   `type(scope): short description` e.g. `style(hero): replace gradient with tiffany-tinted bg`

3. **PR** — run:
   ```
   gh pr create --title '[commit title]' --body '- file.ext: what changed
   - file.ext: what changed' --base main
   ```

4. **Update CLAUDE.md and chat-context.md** — in the same commit if any spec or decision changed. Standard on every prompt.

5. **Update Build Log** — add entry to `## Build Log` in CLAUDE.md:
   `- YYYY-MM-DD | \`branch-name\` | Short summary of what changed`

6. **Never commit directly to main.**

---

## Token Efficiency Rules
- No explanations unless asked. Code only.
- Targeted edits only — never rewrite a full file for a small change.
- Batch all changes to one file in a single operation.
- No preamble, no post-task summaries.
- If a task touches >50 lines, confirm scope first.

---

## Site Structure
```
/
├── index.html
├── about.html
├── services.html
├── contact.html
└── assets/
    ├── css/styles.css
    ├── images/
    └── js/
```

---

## Brand

### Colors
| Token | Hex | Usage |
|---|---|---|
| `--color-primary` | `#8CC5C5` | Tiffany Blue — dominant accent, icons, borders, eyebrows |
| `--color-secondary` | `#C5E2E2` | Light Cyan — backgrounds, badges, hover fills |
| `--color-accent` | `#2E9797` | Dark Cyan — nav, headings, links |
| `--color-cta` | `#FF6F61` | Coral — CTA buttons ONLY, never overuse |
| `--color-cta-hover` | `#CC4F44` | Coral dark — hover state |
| `--color-neutral` | `#575757` | Davy's Gray — ALL body/paragraph text |
| `--color-bg` | `#F4FAFA` | Main bg (white + tiffany tint) |
| `--color-bg-alt` | `#E8F5F5` | Alternating section bg |
| `--color-nav` | `#2E9797` | Navbar |
| `--color-footer` | `#1A3535` | Footer |
| `--color-text-heading` | `#2A4A4A` | h1–h4 |

### Typography
- Georgia, 'Times New Roman', serif — headings AND body. No Google Fonts.
- H1: 48px / H2: 36px / H3: 28px / H4: 22px / Body: 16px / Small: 14px
- Body line-height: 1.75 · Heading line-height: 1.2

### Components
- **Nav:** Sticky, `#2E9797` bg, white links, coral CTA right, `#8CC5C5` 2px bottom border
- **Buttons:** Primary = coral. Secondary = `#8CC5C5` outline. Ghost = white outline on dark bg
- **Cards:** White bg, shadow, 8px radius, `#8CC5C5` top border 4px
- **Sections:** Alternate `#F4FAFA` / `#E8F5F5`
- **Footer:** `#1A3535` bg, `#8CC5C5` top border 3px

---

## Butterfly Animation
- Fixed SVG, `z-index: 9999`, `pointer-events: none`, injected into all 4 pages
- Wings: `#8CC5C5` outer / `#C5E2E2` lower · Body: `#1E6E6E` · Veins: `#2E9797`
- Lissajous flight path (sin/cos), lerp 0.028, scroll drift (scrollY * 0.035)
- CSS wing flap, speed tied to velocity
- Mobile: 36px, upper 40% viewport only · Must not overlap sticky nav

---

## Output Rules
- Always use CSS custom properties — never hardcode hex values
- Match existing class naming conventions
- Clean production-ready code, no inline comments unless asked