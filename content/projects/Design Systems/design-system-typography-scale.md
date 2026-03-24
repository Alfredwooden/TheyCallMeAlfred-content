---
id: design-system-typography-scale
title: Typography Scale System
description: A comprehensive typography system with semantic text styles and headline hierarchy that adapts beautifully across all device sizes.
tags:
  - Typography
  - Text Styles
  - Headlines
  - Font Hierarchy
date: May 2024
status: completed
---

## Overview

Typography is the most underestimated part of a design system. Get it wrong and everything feels inconsistent, even if the colors and spacing are perfect. I built this scale to give every text element a clear role — something you can name without describing the font size.

The system uses semantic class names instead of size utilities. `.headline-hero` is for a page's primary heading. `.text-body` is for reading prose. `.text-code` is for monospaced content. You don't need to know that one is 48px and the other is 16px — the names tell you when to use them.

## How It Works

The scale is defined using CSS custom properties at the `:root` level. Each type style is a class that applies `font-size`, `line-height`, `font-weight`, and `letter-spacing` together as a unit. Changing a breakpoint adjusts the whole scale proportionally — you never end up with a heading that's 48px on desktop but still 48px on a phone.

Responsive scaling uses `clamp()` so sizes transition smoothly between breakpoints instead of jumping at a fixed pixel threshold.

## Headline Hierarchy

The headline scale has six levels, each with a distinct visual weight:

- **headline-hero** — top-level page heading, large and bold
- **headline-group** — section heading within a page
- **headline-block** — subsection heading
- **headline-minor** — tertiary heading, same weight as body but larger
- **headline-label** — eyebrow text above a section, all-caps, tracked out
- **headline-caption** — small label below a visual element

## Text Styles

Body text comes in three sizes — `.text-lead` for introductory paragraphs, `.text-body` for standard reading, and `.text-small` for supporting information. Code styles (`.text-code`, `.text-code-small`, `.text-tiny`) use a monospaced stack and slightly tighter tracking.
