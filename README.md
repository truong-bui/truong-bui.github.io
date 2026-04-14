# Truong Bui - Portfolio

Personal portfolio website showcasing my game development projects built with Unreal Engine and Unity.

**Live site:** [https://truong-bui.github.io](https://truong-bui.github.io)

## Tech Stack

- [Astro](https://astro.build/) - Static site generator
- [MDX](https://mdxjs.com/) - Content authoring with components
- GitHub Pages - Hosting
- GitHub Actions - CI/CD

## Getting Started

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Project Structure

```
src/
├── components/         # Reusable UI components
│   ├── Gallery.astro       # Image gallery with lightbox
│   ├── ProjectCard.astro   # Project card for the homepage grid
│   └── YouTube.astro       # Responsive YouTube embed
├── content/
│   └── projects/       # Project pages (.mdx)
├── layouts/
│   ├── BaseLayout.astro    # Site-wide layout (header, footer, SEO)
│   └── ProjectLayout.astro # Project detail page layout with author sidebar
├── pages/
│   ├── index.astro         # Homepage
│   ├── 404.astro           # 404 page
│   └── [slug].astro        # Dynamic route for project pages
├── styles/
│   └── global.css          # Global styles and CSS variables
└── content.config.ts   # Content collection schema
public/
├── images/             # Project screenshots and assets
├── favicon.ico
└── robots.txt
```

## Adding a New Project

Create a new `.mdx` file in `src/content/projects/`:

```mdx
---
title: My New Project
slug: my-new-project
year: 2024
image: /images/my-project/thumbnail.png
excerpt: "UE5 Game | C++"
---

## Project description

Write your project description here. You can use Markdown and import Astro components:

import YouTube from '../../components/YouTube.astro';
import Gallery from '../../components/Gallery.astro';

<YouTube id="your-video-id" />
<Gallery images={[{ src: '/images/my-project/screenshot.png' }]} />
```

The project will automatically appear on the homepage under the correct year.

## Deployment

The site deploys automatically to GitHub Pages via GitHub Actions on every push to `main`. To set up:

1. Go to **Settings > Pages** in your GitHub repository
2. Set **Source** to **GitHub Actions**
