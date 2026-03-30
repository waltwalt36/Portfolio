# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev    # Development server with hot reload (nodemon)
npm start      # Production server
```

Server runs on port 3000 by default (or `PORT` env variable).

## Architecture

**Express + EJS single-page portfolio.** No build step — changes to CSS/JS/EJS are reflected immediately on page reload (or server restart for EJS).

- `server.js` — Minimal Express setup: static files from `/public`, single `GET /` route rendering `views/index.ejs`
- `views/index.ejs` — The entire page; all sections (hero, about, projects, experience, contact) live here as a single scrollable template
- `public/css/style.css` — All styling; uses CSS custom properties for the color system (brown/tan/green/cream palette); mobile breakpoint at 900px
- `public/js/main.js` — Client-side JS: custom cursor, IntersectionObserver scroll-reveal animations, active nav highlighting

## Deployment

- **Vercel**: `vercel.json` routes all requests through `server.js` via `@vercel/node`
- **Railway/Heroku**: `Procfile` defines `web: node server.js`
