# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for "Nýdecký Revival", a worship evening event organized by SCEAV Bystřice church in Czech Republic. The site showcases event information and provides social media links. It's a Firebase-hosted single-page application with a minimal, elegant design featuring a central poster image with informational panels on the sides.

## Technology Stack

- **Static HTML/CSS/JavaScript**: Pure web technologies, no build process required
- **Firebase Hosting**: Configured through `firebase.json`
- **External Resources**: Font Awesome icons, Google Fonts (Oswald, Anton, Bebas Neue, Impact)
- **Responsive Design**: CSS Grid layout with mobile-first responsive breakpoints

## Project Structure

```
revival/
├── firebase.json          # Firebase hosting configuration
└── public/               # Static site files (served by Firebase)
    ├── index.html        # Main HTML page (Czech language)
    ├── style.css         # All styling and responsive design
    ├── revival.jpg       # Event poster image
    ├── favicon files     # Various favicon formats
    ├── robots.txt        # SEO configuration
    └── sitemap.xml       # SEO sitemap
```

## Architecture

The site uses a **three-panel CSS Grid layout**:
- **Left Panel**: Event information (about the revival)
- **Center Panel**: Featured poster image with 3D hover effects
- **Right Panel**: Social media links (YouTube, Instagram, Facebook, SCEAV)

### Key Design Features

- **3D Transforms**: The poster image has perspective and rotation effects
- **Gradient Backgrounds**: Multi-layered gradients for depth
- **Responsive Layout**: Grid switches to vertical stack on mobile (`@media` queries at 1200px, 950px, 600px)
- **CSS Animations**: Hover effects with cubic-bezier transitions
- **Backdrop Filters**: Blur effects for panels

## Development Commands

Since this is a static site, there are no build commands. For local development:

```bash
# Serve locally (if Firebase CLI is installed)
firebase serve

# Deploy to Firebase
firebase deploy
```

## Content Management

- **Text Content**: All Czech text is directly in `index.html`
- **SEO**: Comprehensive meta tags, Open Graph, Twitter Cards, and JSON-LD structured data
- **Images**: Main poster is `revival.jpg`, optimize before replacing
- **Social Links**: Update URLs in the right panel section

## Styling Notes

- **Primary Colors**: Dark blue-green background (`rgb(40, 65, 70)`), bronze accents (`rgb(130, 90, 30)`)
- **Typography**: "Bebas Neue" for headings, "Inter" for body text
- **Layout**: CSS Grid with `grid-template-columns: 1fr 2fr 1fr`
- **Mobile**: Switches to single column with reordered sections

## Important Files

- `public/index.html:1-196`: Complete site structure and content
- `public/style.css:1-365`: All styling including responsive breakpoints
- `firebase.json:1-16`: Firebase hosting configuration with SPA rewrites