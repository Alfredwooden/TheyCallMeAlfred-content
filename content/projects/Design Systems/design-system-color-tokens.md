---
id: design-system-color-tokens
title: Color Token System
description: My color system that finally solved the "random hex codes everywhere" problem. Built with semantic tokens so switching themes actually works.
tags:
  - Design Tokens
  - Colors
  - Themes
  - CSS Variables
date: May 2024
status: completed
---

## Overview

I built this color system after getting fed up with `#3a7bd5` appearing in 40 different places across a codebase, all meaning slightly different things. The goal was one system where every color has a name that describes what it does, not what it looks like.

The result is a two-tier architecture: core color primitives and semantic tokens. Primitives are the raw palette — Yellow, Blue, Green, Red, Dark, Light, each with five shades (100–500). Semantic tokens map those primitives to specific roles, like `--nadsAccentPrimary` or `--nadsBackground100`. Theme switching just remaps the semantic layer — the primitives never change.

## How It Works

When you switch themes using `theme dark` or `theme matcha` in the console, only the semantic token mappings update. `--nadsAccentPrimary` might point to `--nadsBlue300` in one theme and `--nadsMatcha400` in another. Every component that uses `--nadsAccentPrimary` updates instantly without touching a single line of component CSS.

This separation also makes the system predictable: if you want to change what "primary" means in a new theme, you only need to update one mapping — not hunt through every stylesheet.

## Token Structure

The primitives are intentionally theme-neutral. `--nadsBlue300` is always the same blue regardless of which theme is active. Semantic tokens are the only layer that changes per theme.

For semantic tokens, the naming follows a consistent pattern: `--nads{Category}{Variant}`. Categories include `Accent`, `Background`, `Foreground`, `Status`, and `Border`. This makes autocomplete useful — typing `--nadsAccent` surfaces every accent role immediately.

## Adding a New Theme

To add a new theme, you define a CSS class with overrides for only the semantic tokens. The primitives don't need to be touched. A minimal new theme can be as few as 10–15 token overrides if the defaults are sensible.
