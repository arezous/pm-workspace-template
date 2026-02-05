---
style: design-narrative
audience: UX designers, design reviews, product-design collaboration
max-length: User journey focused, as needed
---

# Design Narrative

> For UX discussions, design reviews, and product-design collaboration.

## When to Use

- Design review presentations
- UX research shareouts
- User journey documentation
- Interaction design specs
- Accessibility reviews
- Any document where the user experience is the focus

## Structure

1. **User problem** — Who is struggling and why, grounded in research
2. **Current experience** — What happens today (pain points, friction)
3. **Journey map** — Step-by-step user flow from trigger to outcome
4. **Proposed experience** — How the new design solves the problem
5. **Interaction flows** — Key screens, states, transitions
6. **Accessibility** — How this works for all users
7. **Open questions** — Areas needing design exploration or testing

## Language Guidelines

- User-centric: "The user sees..." not "The system displays..."
- Empathetic: acknowledge frustration, confusion, delight
- Experience-focused: describe what it feels like, not just what it does
- Grounded in research: reference real user quotes, observations, data

## Tone

Empathetic, story-driven. Put the reader in the user's shoes.

## Avoid

- Technical implementation details (how the backend works)
- Business metrics and revenue projections
- Jargon that distances from the human experience
- Describing interfaces without describing the user's mental model

## Examples

### Bad

> The modal component renders a form with email and password fields. On submit, the API validates credentials and returns a JWT token. Error states display inline validation messages.

### Good

> **Today:** Sara opens the app for the first time. She sees a login screen with no context about what the app does. She hasn't created an account yet, but the "Sign Up" link is buried below the fold. She taps "Login," gets an error, feels confused, and closes the app.
>
> **Proposed:** Sara opens the app and sees a 3-screen welcome flow showing key features. The primary action is "Get Started" (account creation). Login is available but secondary. Sara creates an account in 2 taps using her Google account. She lands on a personalized home screen with a guided first action.
>
> **Key transition:** Confusion ("what is this?") becomes confidence ("I know what to do next")

## Template Reference

Use this style with any template by adding to the YAML frontmatter:

```yaml
output-style: design-narrative
```
