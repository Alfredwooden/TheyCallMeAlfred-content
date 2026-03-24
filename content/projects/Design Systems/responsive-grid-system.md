---
id: responsive-grid-system
title: Responsive Grid System
description: A 12-column grid that actually works on every device. Built with flexbox and responsive gutters that adapt from mobile to desktop.
tags:
  - Grid System
  - Layout
  - Responsive
  - Flexbox
date: May 2024
status: completed
---

## Overview

I built this grid system because I kept reinventing the same 12-column layout in every project. I wanted something predictable, easy to reason about, and consistent with how designers think about layouts — without pulling in a full framework just to get columns.

The system uses flexbox under the hood with a token-driven gutter that narrows on mobile and opens up on larger screens. No JavaScript, no calculations at runtime — just CSS classes that describe what you want.

## How It Works

Layouts are built with three classes: `.container` sets the max-width and horizontal padding, `.row` establishes the flex context and negative margins to offset gutters, and `.col-{n}` sets the width as a percentage of 12 columns.

Responsive variants follow the same pattern with a breakpoint suffix: `.col-sm-12`, `.col-md-6`, `.col-lg-4`. Columns stack to full-width on mobile by default unless you specify a `.col-sm-*` override.

## Breakpoints

The system uses four breakpoints defined as CSS custom properties so they can be referenced consistently across the codebase:

- **sm** — 576px and up (large phones, landscape)
- **md** — 768px and up (tablets)
- **lg** — 992px and up (laptops)
- **xl** — 1200px and up (desktops)

## Offsets and Nesting

Columns can be offset with `.col-offset-{n}` to push them right without adding an empty column. Rows can be nested inside columns — the inner row gets its own gutter context, so gutters don't compound.

This covers about 95% of real-world layout needs without needing any custom positioning logic.
