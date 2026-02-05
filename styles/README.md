# Output Styles

Output styles control how your documents are written depending on the audience. The same information — a feature launch, a product decision, a status update — reads differently for an executive than for an engineer.

## How It Works

Each style guide defines:
- **Audience** — Who is reading this
- **Length** — How long it should be
- **Structure** — How to organize the content
- **Language** — What kind of words to use
- **Tone** — How it should feel
- **Examples** — Good vs bad formatting

## Available Styles

| Style | Audience | Length | Use When |
|-------|----------|--------|----------|
| [executive-brief](executive-brief.md) | Leadership, board | 500-600 words | Decision requests, board updates, strategy proposals |
| [engineering-spec](engineering-spec.md) | Dev teams, QA | As needed | Feature handoffs, technical designs, sprint planning |
| [design-narrative](design-narrative.md) | UX, design reviews | Journey-focused | Design reviews, UX research, interaction specs |
| [slack-update](slack-update.md) | Team, stakeholders | 3 bullets, <200 words | Standups, shipping updates, blocker flags |

## Using Styles with Templates

Reference a style in any template's YAML frontmatter:

```yaml
---
title: 'Search v2'
type: 'One-Pager PRD'
output-style: executive-brief
---
```

When drafting with Claude Code, reference the style directly:

```
"Write a status update for the search project using the slack-update style"
```

```
"Convert this PRD into an executive-brief for the leadership review"
```

## Adding New Styles

Create a new markdown file in `styles/` following the same structure:

1. YAML frontmatter with `style`, `audience`, and `max-length`
2. Description of when to use it
3. Structure, language, and tone guidelines
4. Good vs bad examples
5. Update this README with the new style
