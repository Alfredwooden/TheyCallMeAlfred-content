# Content Styleguide

This guide defines the conventions for all markdown files in this repo. Every entry — whether a project or a playground item — must follow this format so the portfolio renders it correctly.

---

## File Naming

- Use the item's `id` value as the filename: `{id}.md`
- Lowercase, hyphen-separated: `not-a-design-system.md`
- Place under the correct folder: `content/projects/` or `content/playground/`

---

## Frontmatter

Every file starts with a YAML frontmatter block. Required fields are marked with `*`.

```yaml
---
id: *           # Unique identifier. Lowercase, hyphen-separated. Never change once published.
title: *        # Display title shown on cards and modals.
description: *  # One or two sentences shown on the card and at the top of the modal.
tags: *         # List of 3–6 short labels. First two appear on the card preview.
date: *         # Human-readable month + year: "March 2024"
status: *       # One of: completed | in-progress | experimental | prototype
category:       # One of: design-systems | experiments | prototypes | tools (omit for general projects)
image:          # Absolute URL to a cover image (optional)
primaryActionLink:    # URL for the primary CTA button, e.g. live demo (optional)
secondaryActionLink:  # URL for the secondary CTA button, e.g. GitHub repo (optional)
---
```

### Rules

- `id` must be unique across both `projects/` and `playground/`. Once a file is published, never change the id — it's used as a key throughout the app.
- `description` is plain text only — no markdown, no HTML. Keep it under 180 characters.
- `tags` should be Title Case: `React`, `Design Tokens`, `TypeScript`. Aim for 3–6.
- `date` is display text, not a machine date. Write `May 2024`, not `2024-05-01`.
- `status` drives the tooltip badge on the card — choose the most accurate value.

---

## Content Body

The body below the frontmatter becomes the modal content. It is rendered as HTML, so standard markdown applies.

### Heading Hierarchy

Use `##` for top-level sections. Use `###` for subsections within a section. Never use `#` (reserved for the document title, which comes from `title` in frontmatter).

```markdown
## What I Built

Introductory paragraph here.

### Technical Details

More specific information here.
```

### Required Sections

**For projects**, include these sections in order:

1. **What I Was Going For** — the motivation and overall goal. Personal, first-person voice.
2. **Key Features** — bullet list of 4–6 features. Bold the feature name, follow with a short description.
3. **Tech Stack** — bullet list of technologies used. Bold the name, follow with the role it played.
4. **Development Challenges** — what was hard and how you solved it.
5. **What I Learned** — honest reflection. Can be short.
6. **Future Enhancements** *(optional)* — bullet list of planned improvements.

**For playground items**, include these sections in order:

1. **Overview** — what the piece is and why it exists. 1–2 paragraphs.
2. **How It Works** — the approach or system explained concisely.
3. Any additional sections relevant to the piece (e.g. breakpoints, token structure, hierarchy).

---

## Writing Style

- **Voice:** First-person, conversational. Write like you're explaining it to a fellow developer over coffee — not a product page.
- **Tone:** Direct and honest. It's okay to say "I was tired of X" or "this was harder than expected."
- **Length:** Sections should be 1–3 paragraphs. Prefer depth over breadth — fewer sections written well beats many shallow ones.
- **Bold:** Use `**bold**` for proper nouns (library names, component names, token names) and feature/tech names in lists. Don't bold for emphasis in prose.
- **Code:** Use backtick inline code for token names, class names, commands, and variable names: `--nadsAccentPrimary`, `press 'c'`, `theme dark`.
- **Lists:** Use bullet lists for features and tech stacks. Use prose paragraphs for narrative sections. Don't bullet everything.

---

## Full Example

```markdown
---
id: my-new-project
title: My New Project
description: A short, plain-text description shown on the card. Under 180 characters.
tags:
  - React
  - TypeScript
  - Design Tokens
date: January 2025
status: completed
category: tools
primaryActionLink: https://my-live-demo.com
secondaryActionLink: https://github.com/me/my-new-project
---

## What I Was Going For

I built this because I kept running into the same problem across projects — no good tool existed for X. So I made one that does exactly what I needed without the overhead of the existing solutions.

## Key Features

- **Fast Setup** — zero configuration needed to get started
- **Token-Driven** — all styles controlled via `--nads*` CSS variables
- **Framework Agnostic** — works in React, Vue, or plain HTML

## Tech Stack

- **React** — component architecture and state management
- **TypeScript** — type safety across the entire codebase
- **Vite** — build tooling and dev server

## Development Challenges

The hardest part was getting the X behaviour to work across Y edge cases. I ended up rebuilding the approach entirely after the first attempt hit a wall with Z.

## What I Learned

Scope creep is real. I started with five features and shipped two well instead of five half-baked ones. That was the right call.

## Future Enhancements

- Add support for dark mode overrides
- Publish as an npm package
```
