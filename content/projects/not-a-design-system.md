---
id: not-a-design-system
title: NADS - Not A Design System
description: A comprehensive design system built with StencilJS, featuring design tokens, multi-theme support, and framework-agnostic components.
tags:
  - Design System
  - StencilJS
  - Design Tokens
  - Component Library
  - Theming
category: design-systems
date: March 2024
status: completed
---

## Overview

NADS (Not A Design System) is a comprehensive design system built with StencilJS that provides framework-agnostic components and a robust theming system. It features design tokens, multi-theme support, and components that work across React, Vue, and vanilla JavaScript.

## Key Features

- **Framework Agnostic** - StencilJS components work in any framework
- **Design Tokens** - Comprehensive token system for consistent theming
- **Multi-Theme Support** - Light, dark, and custom themes
- **Accessible** - Built with WCAG guidelines from the ground up
- **Type Safe** - Full TypeScript support with proper type definitions

## Technical Architecture

The system is built on StencilJS, which compiles to standard web components that work anywhere. The design token pipeline transforms Figma tokens into CSS variables that power the entire component library.

```
Figma (Token Studio) → JSON → CSS Variables → Components
```

## Component Library

The system includes a comprehensive set of components including buttons, forms, navigation, data display, and layout components. Each component is designed to be flexible and themeable through the token system.

### For Developers

- Consistent component API
- Framework agnostic
- Type-safe development
- Automated testing

### For Designers

- Visual consistency
- Token-based theming
- Figma integration
- Living documentation
