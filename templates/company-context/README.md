# Company Context Templates

Templates for documenting your company, product, customers, and competitive landscape. This shared context helps Claude (and your team) make better product decisions grounded in real business knowledge.

## What's in This Folder

| Template | Purpose | Update Frequency |
|----------|---------|-----------------|
| [COMPANY.md](COMPANY.md) | Company overview, stage, strategy, and constraints | Quarterly |
| [PRODUCT.md](PRODUCT.md) | Product details, tech stack, metrics, and architecture | Quarterly |
| [PERSONAS.md](PERSONAS.md) | Customer personas, jobs to be done, and behavior patterns | Quarterly |
| [COMPETITIVE.md](COMPETITIVE.md) | Competitive landscape, feature matrix, and win/loss analysis | Quarterly |

## How to Use These Templates

### 1. Copy and Fill
Copy each template into your project's working directory and replace the bracketed placeholders with your actual information:

```
cp templates/company-context/COMPANY.md company-context/COMPANY.md
cp templates/company-context/PRODUCT.md company-context/PRODUCT.md
cp templates/company-context/PERSONAS.md company-context/PERSONAS.md
cp templates/company-context/COMPETITIVE.md company-context/COMPETITIVE.md
```

### 2. Start With What You Know
You don't need to fill every field on day one. Start with the sections you can complete confidently and mark unknowns with `[TBD]`. A partially filled template is far more useful than no template at all.

### 3. Use With Claude
Reference these documents when working with Claude on product tasks:

- **PRD writing:** Claude uses company context to set realistic scope and align with strategy
- **Prioritization:** Persona data and competitive analysis inform tradeoff decisions
- **Research:** Market position and constraints shape the right questions to ask
- **Roadmap planning:** Strategic priorities and business metrics guide sequencing

## How Company Context Connects to Other Areas

### `.claude/` Directory
Place completed company context files in your project's `.claude/` directory (or reference them from `CLAUDE.md`) so Claude automatically has access to your business context in every conversation.

```
.claude/
  CLAUDE.md          # References company-context files
  company-context/   # Filled-in versions of these templates
    COMPANY.md
    PRODUCT.md
    PERSONAS.md
    COMPETITIVE.md
```

### `research/` Directory
Company context informs and is informed by research:

- **Personas** should be updated when new customer research lands in `research/`
- **Competitive analysis** should reflect findings from market research
- **Business metrics** in COMPANY.md may reference data from research reports

### `templates/prds/`
PRD templates reference company context to ensure product decisions align with company strategy, target the right personas, and account for competitive dynamics.

## Maintenance Schedule

### Quarterly Reviews (Recommended)
Set a recurring calendar reminder to review all four documents:

- [ ] **COMPANY.md** — Update metrics, strategic priorities, and any stage changes
- [ ] **PRODUCT.md** — Update features, metrics, tech stack changes, and version info
- [ ] **PERSONAS.md** — Incorporate new customer research and update the comparison matrix
- [ ] **COMPETITIVE.md** — Refresh competitor data, update win/loss analysis, and check for new entrants

### Trigger-Based Updates
Update immediately when:

- A new funding round closes or company stage changes
- A major product launch or pivot occurs
- Significant customer research is completed
- A competitor makes a major move (acquisition, new product, pricing change)
- Win/loss patterns shift noticeably

## Tips for Keeping Documents Current

1. **Assign owners.** Each document should have a single person responsible for keeping it up to date. Shared responsibility often means no one updates it.

2. **Make it a habit.** Add a 15-minute "context review" to your quarterly planning process. Most updates are small.

3. **Link to sources.** When you add metrics or claims, link to the source (dashboard, report, Slack thread). This makes future updates faster.

4. **Be honest about unknowns.** Mark fields as `[TBD]` or `[Needs research]` rather than guessing. Inaccurate context is worse than missing context.

5. **Keep it concise.** These are working reference documents, not exhaustive reports. If a section grows beyond a few bullet points, consider linking to a separate deep-dive document instead.

6. **Version with git.** Track changes to these documents in version control. The diff history tells the story of how your understanding evolved.
