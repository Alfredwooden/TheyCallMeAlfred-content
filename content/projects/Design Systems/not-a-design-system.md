---
id: not-a-design-system
title: NADS - Not A Design System
description: I kept copying the same styles from project to project and getting inconsistent results. NADS is the one source of truth I actually use.
tags:
  - Design System
  - StencilJS
  - Design Tokens
  - Component Library
  - Theming
date: March 2024
status: completed
category: design-systems
secondaryActionLink: https://github.com/Alfredwooden/not-a-design-system
---

## What I Was Going For

I built NADS because I kept copying the same color variables and button styles from project to project and getting inconsistent results every time. I wanted one source of truth — something I could install and trust to look the same whether I was in React, Vue, or plain HTML.

The name is a bit of a joke. Every design system claims not to be a design system until it becomes one. This one leans into that.

## Key Features

- **Framework Agnostic** — StencilJS compiles to standard web components that work anywhere
- **Design Tokens** — comprehensive token system for consistent theming across all components
- **Multi-Theme Support** — ships with light, dark, high-contrast, cream, sunset, ocean, and matcha themes
- **Accessible** — built with WCAG guidelines from the ground up
- **Type Safe** — full TypeScript support with proper type definitions
- **Token Pipeline** — Figma (Token Studio) → JSON → CSS variables → components

## Tech Stack

- **StencilJS** — compiles to native web components with zero runtime dependency
- **TypeScript** — strict typing across every component and utility
- **CSS Variables** — all visual properties driven by `--nads*` tokens so themes swap cleanly
- **Token Studio** — Figma plugin that exports the token JSON consumed by the build pipeline

## Development Challenges

Getting the token pipeline right took a few iterations. The first version had tokens that were too granular — I had individual tokens for every state of every component, which made the Figma file a nightmare to maintain. I ended up collapsing them into a two-tier system: core primitives (the actual color values) and semantic tokens (what those colors mean in context). That made everything much easier to reason about.

The other tricky part was making the web components feel native in React without requiring a wrapper library. Stencil handles most of this, but getting event types and ref forwarding to play nicely took some work.

## What I Learned

Semantic naming is hard to get right the first time. `--nadsAccentPrimary` sounds obvious until you're staring at a dark theme and wondering whether "primary" means "most prominent" or "brand colour". Writing the naming conventions down explicitly before building saved a lot of back-and-forth later.

I also learned that the token pipeline is only as good as its documentation. The system works great — but if I didn't document which primitive maps to which semantic token and why, future-me would have no idea why I made those choices.

## Future Enhancements

- Publish the full component library to npm
- Add animation tokens for consistent motion design
- Expand the icon set beyond the current selection
- Build a Storybook integration for interactive component docs
