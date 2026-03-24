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
---

## What I Was Going For

So I built this portfolio website with a super clean black and white look. I've always been drawn to minimalist designs - there's something about stripping away all the unnecessary stuff that just feels right to me. The black and white vibe gives it this timeless feel, plus it makes the content really pop without distractions.

Right now it's a monochrome situation, but I've actually set it up so I can easily swap in different themes later. The whole site is built on top of NADS (Not A Design System), that design system I created. This is where everything comes full circle - all those tokens, themes, and components I built actually get put to use here.

## The Hidden Terminal Console

The coolest part of this site isn't even immediately visible - it's this terminal-style console that I built from scratch. You can press 'c' anywhere on the site and this command console drops down. From there, you can actually change site settings in real-time, like switching between different background animations or toggling themes.

Building that console was a trip. I wanted it to feel like a real terminal, so I added features like command history (press up to cycle through previous commands), draggable window, resizable corners - the whole deal. It's one of those things that was way more complicated than I expected, but super satisfying once I got it working.

The console is actually a perfect showcase for my design system in action. All the styling, from the typography to the button states, is powered by NADS tokens. When you switch themes in the console, you're actually seeing my token-based theming system at work - all those components update instantly without any style recalculation.

### Available Console Commands

- `help` - List all available commands
- `theme [mode]` - Get or set theme (light|dark|highcontrast|cream|sunset|ocean|matcha)
- `clear` - Clear console history
- `animations` - Switch background animation mode

## Dynamic Background Animations

I've got these subtle background animations happening behind everything - either floating particles or this grid of animated dots. They're not in-your-face, but they add this nice sense of depth and movement to what would otherwise be a static page.

You can actually swap between different animation modes through that console I mentioned. Just type "animations particles" or "animations dots" and watch the background transform. It's these little interactive touches that make a site feel more alive and personal, you know?

## Technical Architecture

Another challenge was setting up the site architecture to support microfrontends. I haven't fully implemented any separate microfrontends yet, but the foundation is there. The idea is that different sections of my portfolio (like the projects showcase, blog, etc.) could actually be completely separate applications that just get stitched together into one seamless experience.

If you dig into the code, you'll see I'm using single-spa as the framework for this. It's like this orchestration layer that can load different React applications on the fly - pretty neat for something that looks so simple on the surface.

## The Tech Stack

- **React** - Main UI library for component-based architecture
- **Vite** - Lightning-fast build tool and dev server
- **SCSS** - Styling with variables and mixins
- **NADS** - My custom design system for components and theming
- **single-spa** - Microfrontend orchestration framework

## Development Challenges

That console was definitely the trickiest part to get right. I wanted it to feel like a proper desktop application window within the browser - something you could move around, resize, and interact with naturally. Getting all those interactions to feel smooth took some doing.

Creating intuitive command parsing was another interesting challenge. The console needed to understand various command formats, provide helpful error messages, and maintain a history that persists across sessions.

## Key Features

- **Interactive Terminal** - Press 'c' to access the hidden console
- **Dynamic Theming** - Switch between light/dark modes instantly
- **Background Animations** - Multiple animation modes for visual interest
- **Responsive Design** - Works seamlessly across all device sizes
- **Design System Integration** - Powered by NADS tokens and components
- **Microfrontend Ready** - Architecture supports modular expansion

## What I Learned

This project really pushed me to think about user interactions in a different way. Creating that console interface made me appreciate the complexity of building tools that feel intuitive. There's this balance between making something powerful enough to be useful but simple enough that it doesn't require a manual.

I also got a much better understanding of microfrontends and when they make sense to use. It's definitely overkill for a personal site, but it was a perfect playground to experiment with the architecture without the stakes of a production app.

## Future Enhancements

I've got several improvements planned:

- Implementing actual microfrontends for different sections
- Adding more theme options beyond light and dark
- Creating additional animation modes and effects
- Building a filterable project showcase
- Adding subtle sound design for interactions
- Expanding the console with more interactive commands

This portfolio is as much a playground for testing ideas as it is a showcase of my work. It's where my design system gets to shine in a real application, and it'll probably never be "finished" - more like a constant work in progress that evolves as I learn and experiment.
