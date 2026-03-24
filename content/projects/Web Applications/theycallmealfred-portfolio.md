---
id: theycallmealfred-portfolio
title: TheyCallMeAlfred Portfolio
description: My personal portfolio with a clean black & white look and a hidden terminal console. Press "c" to find the secret features.
tags:
  - Portfolio
  - React
  - Minimalist Design
  - Interactive UI
  - Microfrontends
  - Terminal
date: May 2024
status: completed
secondaryActionLink: https://github.com/Alfredwooden/TheyCallMeAlfredViteJS
---

## What I Was Going For

I built this portfolio with a super clean black and white look. I've always been drawn to minimalist designs — there's something about stripping away all the unnecessary stuff that just feels right. The monochrome aesthetic gives it a timeless quality and makes the content pop without distractions.

The whole site is built on top of NADS (Not A Design System), the design system I created. This is where everything comes full circle — all those tokens, themes, and components actually get put to use here in a real application.

## Key Features

- **Interactive Terminal** — press `c` anywhere on the site to open the hidden console
- **Dynamic Theming** — switch between light, dark, matcha, and more from the console
- **Background Animations** — multiple animation modes (particles or dots) switchable at runtime
- **Responsive Design** — works seamlessly across all device sizes
- **Design System Integration** — powered entirely by NADS tokens and components
- **Microfrontend Ready** — architecture built on single-spa for modular expansion

## Tech Stack

- **React** — component architecture and UI layer
- **Vite** — build tooling and dev server
- **SCSS** — styling with variables and mixins layered on top of NADS tokens
- **NADS** — my custom design system for all components, typography, and theming
- **single-spa** — microfrontend orchestration framework
- **Redux Toolkit** — persistent state management for theme and UI preferences

## Development Challenges

The terminal console was definitely the trickiest part. I wanted it to feel like a real desktop application window — something you could move around, resize, and interact with naturally. Getting drag-and-resize to feel smooth, handling edge cases at the viewport boundary, and making sure it didn't interfere with the rest of the page's keyboard navigation took more time than I expected.

Command parsing was another interesting challenge. The console needed to understand various input formats, give helpful error messages for typos, and maintain a command history that cycles on arrow-up. Getting that to feel natural without writing an actual shell parser was a fun constraint.

Setting up the single-spa architecture was also more involved than it looks. The foundation is there for loading separate microfrontend apps, but wiring up the shared dependencies and making sure NADS loaded once (not once per microfrontend) required careful configuration.

## What I Learned

This project pushed me to think about user interactions differently. Building the console made me appreciate how much work goes into making a tool feel intuitive — there's a balance between powerful enough to be useful and simple enough that it doesn't need a manual.

I also got a much better understanding of when microfrontends make sense. It's overkill for a personal site, but it was a perfect low-stakes playground to experiment with the architecture.

## Future Enhancements

- Implement actual microfrontends for different portfolio sections
- Add more theme options and a theme preview in the console
- Build a filterable project showcase with tag-based filtering
- Expand the console with more interactive commands
- Add subtle sound design for interactions
