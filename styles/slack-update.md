---
style: slack-update
audience: Team, cross-functional stakeholders
max-length: 3 bullets, under 200 words
---

# Slack Update

> For quick team updates in Slack, Teams, or any chat channel.

## When to Use

- Daily or weekly standups
- Shipping announcements
- Quick progress updates
- Flagging blockers to the team
- Any update that should take 10 seconds to read

## Structure

Three bullets, always in this order:

1. **Shipped** — What got done
2. **Next** — What's coming
3. **Blockers** — What's stuck (omit if none)

## Language Guidelines

- Casual and clear
- Emoji-friendly for scannability
- Link to details instead of explaining in-line
- Specific: names, numbers, dates

## Tone

Conversational, brief. Write like you're talking to a teammate.

## Avoid

- Formal language or corporate speak
- Long explanations or justifications
- Paragraphs (if it's more than 3 lines, it's too long)
- Ambiguous timelines ("soon", "shortly")

## Examples

### Bad

> Hi team, I wanted to give you an update on the project. We've been making good progress this week. The team has been working hard on the search feature and we're hoping to have it ready soon. There are some dependencies we're working through but overall things are going well. I'll keep you posted on next steps.

### Good

> **Search v2 update:**
> - Shipped: Autocomplete + filters live in staging, QA started
> - Next: Production deploy Thursday, monitoring through Friday
> - Blocker: Need API rate limit increase from platform team — @jake can you approve?

### Also Good (no blockers)

> **Onboarding redesign:**
> - Shipped: New welcome flow live for 10% of users
> - Next: Ramp to 50% Monday, full rollout if metrics hold

## Template Reference

Use this style with any template by adding to the YAML frontmatter:

```yaml
output-style: slack-update
```
