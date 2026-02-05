---
style: engineering-spec
audience: Dev teams, technical reviewers, QA
max-length: As needed for complete specification
---

# Engineering Spec

> For dev teams, technical reviews, and implementation planning.

## When to Use

- Handing off features to engineering
- Technical design discussions
- Sprint planning and backlog refinement
- API and integration specifications
- Any document where developers are the primary audience

## Structure

1. **Overview** — What we're building and why (1-2 sentences)
2. **Requirements** — Functional and non-functional, numbered for reference
3. **Acceptance criteria** — Testable conditions for "done"
4. **Technical details** — Architecture, APIs, data models, dependencies
5. **Edge cases** — What happens when things go wrong
6. **Out of scope** — Explicitly state what this does NOT include
7. **Open questions** — Unresolved decisions that need input

## Language Guidelines

- Technical precision: name specific systems, APIs, and data types
- Implementation details welcome and expected
- Reference existing code, services, and infrastructure by name
- Use numbered requirements for easy reference in reviews

## Tone

Precise, detailed, thorough. Assume the reader will build exactly what you write.

## Avoid

- Ambiguity ("should handle errors appropriately" — which errors? how?)
- Missing edge cases
- Incomplete specs that require guesswork
- Business justification (that belongs in the PRD)
- Marketing language

## Examples

### Bad

> The search feature should be fast and return relevant results. It should handle errors gracefully and work on mobile.

### Good

> **REQ-1:** Search returns results within 200ms (p95) for queries up to 100 characters
>
> **REQ-2:** Results ranked by relevance score (TF-IDF) with recency boost (0.1x per day decay)
>
> **REQ-3:** Empty query state shows top 10 trending searches from the past 24h
>
> **Edge cases:**
> - Query timeout (>2s): Show cached results with "Results may be outdated" banner
> - Zero results: Show "No results for [query]" with 3 suggested alternative queries
> - Service unavailable: Degrade to client-side filtering of cached catalog data
>
> **Acceptance criteria:**
> - [ ] Search returns results for all supported languages (EN, SV, DE)
> - [ ] Results pagination loads next 20 items on scroll
> - [ ] Query with special characters (!@#$) does not cause 500 error

## Template Reference

Use this style with any template by adding to the YAML frontmatter:

```yaml
output-style: engineering-spec
```
