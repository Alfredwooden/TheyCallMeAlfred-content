# How I Write Content For This Site

This is the format I use for every entry in this repo — projects and playground items. If it doesn't follow this, the site won't render it properly. Future me, don't skip this.

---

## File naming

Name the file after the `id` you pick, all lowercase with hyphens. So if the id is `not-a-design-system`, the file is `not-a-design-system.md`.

Put it in the right folder:
- New project → `content/projects/Your Section Name/`
- New playground item → `content/playground/Your Section Name/`

The folder name becomes the section title on the site, so make it readable — `Design Systems` not `design-systems`.

---

## The bit at the top of every file

Every file starts with this block. Fill it in before writing anything else.

```yaml
---
id: my-project-name
title: My Project Name
description: One or two sentences. This shows up on the card and at the top of the modal.
tags:
  - React
  - TypeScript
  - Something Else
date: January 2025
status: completed
---
```

**What each field does:**

- **id** — pick something short and descriptive, lowercase with hyphens. Never change it once the file is live, it's how the app tracks the entry.
- **title** — what shows on the card.
- **description** — plain text only, no formatting. Keep it under 180 characters. Write it like a one-liner pitch, not a job description.
- **tags** — Title Case, 3 to 6 of them. The first two show on the card preview, the rest appear in the modal.
- **date** — write it human-readable: `May 2024`, not `2024-05-01`.
- **status** — pick the closest one: `completed`, `in-progress`, `experimental`, or `prototype`. This shows up as a badge on the card.

**Optional extras** (add these only if you have them):

```yaml
category: design-systems       # or: experiments | prototypes | tools
image: https://...             # cover image URL
primaryActionLink: https://... # live demo button
secondaryActionLink: https://... # github repo button
```

---

## Writing the content

Everything below the `---` closing line is the content that appears in the modal when someone clicks the card. Write it in markdown.

**Start sections with `##`** — that's the biggest heading you should use here. The page title already comes from the `title` field, so don't repeat it. Use `###` if you need a subsection inside a section.

---

## What to write for a project

Keep this order. Not every section needs to be long — a short honest paragraph beats two padded ones.

**1. What I Was Going For**
Why did I build this? What problem was I trying to solve, or what did I want to learn? Write it like I'm explaining it to someone over coffee. First person, no fluff.

**2. Key Features**
A bullet list of the things worth calling out. Bold the feature name, then a short description after a dash:
```
- **Feature Name** — what it does and why it matters
```

**3. Tech Stack**
Same format as features — bold the tool, then what I used it for. Don't just list names, say what role each one played.

**4. Development Challenges**
The honest part. What was actually hard? What broke? What did I have to rebuild? This is the most interesting section — don't skip it or sugarcoat it.

**5. What I Learned**
Short reflection. One or two paragraphs is fine. What would I do differently? What clicked?

**6. Future Enhancements** *(only if I actually plan to do them)*
A bullet list of what's next. Don't add this section just to have it.

---

## What to write for a playground item

Playground items are smaller, more focused things. Usually a piece of a design system or an experiment.

**1. Overview**
What is this thing and why does it exist? One or two paragraphs.

**2. How It Works**
The interesting part — the approach, the system, the decisions I made. Keep it focused.

After that, add whatever sections make sense for the piece. For a color system that might be "Theme Colors" and "Core Primitives". For a grid system it might be "Breakpoints" and "Spacing". Use judgment.

---

## Section descriptions

To add a description under a section heading (like "Design Systems"), drop an `_index.md` file in that folder. Just write the description as plain text — no frontmatter needed, no headings. It'll show up on the site as the section intro.

---

## A few writing rules I want to stick to

- Write in first person. This is my portfolio, not a product page.
- Be honest. If something was hard, say it was hard. If I'd do it differently, say that too.
- Keep sections tight. 1–3 paragraphs per section is the sweet spot. If I'm writing more than that, I'm probably padding.
- **Bold** for tool names and feature names in lists. Not for emphasis in normal sentences.
- Use `backtick code` for anything you'd type: command names, token names, class names, file names.
- Bullet lists for features and stacks. Paragraphs for everything else. Don't turn the whole thing into a list.

---

## Quick example

```markdown
---
id: my-new-tool
title: My New Tool
description: A thing I built because I kept hitting the same frustrating problem and couldn't find anything that handled it well.
tags:
  - React
  - TypeScript
  - Design Tokens
date: January 2025
status: completed
primaryActionLink: https://my-live-demo.com
secondaryActionLink: https://github.com/Alfredwooden/my-new-tool
---

## What I Was Going For

I built this because I kept running into the same problem — no good tool existed for X. So I made one that does exactly what I needed without the overhead of everything else out there.

## Key Features

- **Fast Setup** — zero configuration, works out of the box
- **Token-Driven** — all styles flow through `--nads*` CSS variables so themes just work
- **Framework Agnostic** — drop it into React, Vue, or plain HTML

## Tech Stack

- **React** — component architecture and state
- **TypeScript** — I'm not going back to untyped code, ever
- **Vite** — build tooling and dev server

## Development Challenges

The tricky part was X. My first approach broke completely when Y happened, so I ended up rebuilding it from scratch with a different mental model. The second attempt was cleaner anyway.

## What I Learned

Scope creep is real. I started with five features and shipped two well instead of five half-baked ones. That was the right call.

## Future Enhancements

- Add dark mode overrides
- Publish to npm
```
