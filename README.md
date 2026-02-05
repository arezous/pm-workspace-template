
# pm-workspace-template

> Building my operating system for AI-native product work

**Status:** v0.2 - Templates and output styles added

---

## What This Is

My personal workspace for doing product management with AI assistance (Terminal + Claude Code + Cursor).

This is a **work in progress**. I'm building it for myself and sharing it publicly as I go.

---

## Current Structure

```
pm-workspace-template/
├── templates/          # PRD, roadmap, update templates
├── frameworks/         # PM methodologies (RICE, OKRs, etc.)
├── automation/         # Export scripts (PDF, DOCX, PPTX)
├── scripts/           # Helper scripts for Terminal
├── .claude/           # Claude Code prompts and preferences
├── styles/            # Communication style guides
├── examples/          # Sample documents
└── docs/             # Documentation
```

---

## Why I'm Building This

I believe every PM will become an AI-powered PM. This is my attempt to figure out what that looks like.

---

## Status

**v0.2** - Templates and output styles added
**v0.1** - Basic structure created
**Next:** Add frameworks and automation scripts

---

## Templates

### PRD Templates
- **one-pager.md** - Concise, problem-first format by [Lenny Rachitsky](https://www.lennysnewsletter.com/p/my-product-spec-template)

More templates coming soon.

---

## Output Styles

Output styles define HOW to format content for different audiences. They're reusable formatting instructions that work across any template.

### Available Styles

- **executive-brief** - For leadership and board (BLUF, 2 pages, business focus)
- **engineering-spec** - For dev teams (technical, detailed, complete specs)
- **design-narrative** - For UX discussions (user-focused, journey-driven)
- **slack-update** - For quick team updates (casual, 3 bullets max)

### How to Use

Reference styles in your document's YAML frontmatter:
```yaml
---
title: 'My PRD'
template: 'one-pager'
style: 'executive-brief'
---
```

Or ask Claude to apply a style:
- "Write this PRD using executive-brief style"
- "Convert this to engineering-spec style"

See [styles/README.md](styles/README.md) for detailed formatting rules.

---

## Contact

Building in public. Questions or feedback welcome.

**Arezou Solouki**  
[LinkedIn](https://www.linkedin.com/in/arezousolouki/) | [Website](https://solouki.se) | arezou@solouki.se

---

**License:** MIT"