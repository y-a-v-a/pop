# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Pop is an interactive web art project created by ax710.org and y-a-v-a.org in 2020. It's a client-side only web application that creates an animated, clickable experience with visual elements that transform through multiple stages when interacted with.

## Architecture

This is a pure frontend project with no build process, dependencies, or backend:

- **index.html**: Single-page application with embedded CSS and Schema.org structured data
- **main.js**: Minified JavaScript containing the core animation and interaction logic
- **img/**: Contains SVG and PNG assets for the animation stages (dog001_2020.svg, lichten1.png, lichten2.png, lichten3.png)
- **Favicon assets**: Complete favicon implementation with multiple formats and sizes

## Development Workflow

Since this is a static web project with no build tools:

- **Development**: Open `index.html` directly in a web browser
- **Testing**: Manual testing in browser - no automated test suite
- **No package.json**: No npm scripts or dependencies
- **No build process**: Files are served directly as-is

## Core Functionality

The application creates animated boxes that:
1. Start with the initial dog SVG image
2. Progress through 3 visual stages when clicked (lichten1.png → lichten2.png → lichten3.png)
3. Generate new boxes dynamically with unique CSS keyframe animations
4. Each box has randomized positioning, rotation, and scaling animations

The main.js contains minified code that:
- Calculates maximum boxes based on screen dimensions
- Creates dynamic CSS keyframes for each box instance
- Handles click interactions and stage transitions
- Manages the addition and removal of DOM elements

## Key Technical Details

- Uses CSS custom animations generated at runtime
- Implements accessibility with `prefers-reduced-motion` media query
- Includes comprehensive favicon support
- Features Schema.org structured data for SEO
- Pure vanilla JavaScript with no frameworks or libraries