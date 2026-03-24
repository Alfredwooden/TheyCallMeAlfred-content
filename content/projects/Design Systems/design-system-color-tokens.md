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

## Token-Based Color System

I built this color system using a two-tier approach: core color primitives (Yellow, Blue, Green, Red, Dark, Light) with 100-500 shades, and semantic tokens that map to specific use cases. This separation makes theme switching a breeze and keeps colors consistent across components - no more random color values scattered throughout the codebase!

## Theme Colors

Semantic tokens like `--nadsAccentPrimary` and `--nadsBackground100` that automatically adapt to different themes while keeping their meaning consistent. It's like having a translator that always knows what "primary button" should look like, regardless of the theme.

## Core Color Primitives

These are my base colors with consistent shade variations (100-500) that serve as the foundation for all semantic tokens. They stay the same across themes, so I never have to worry about breaking anything when switching between light and dark modes.

## How Theme Switching Works

When you switch themes in my console (press 'c' and try "theme dark" or "theme matcha"), only the semantic token mappings change. The core primitives stay the same, but `--nadsAccentPrimary` might switch from pointing to `--nadsBlue300` in light theme to `--nadsRed300` in dark theme. This keeps everything consistent while completely transforming the visual experience.
