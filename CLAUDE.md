# Flip Finance — Business/Client Project (Hands-Off)

## Overview
Financing website for a real estate company. Simple landing page with contact and financing application forms that submit to GoHighLevel via webhooks.

## Project Status: Business/Client
- **Owner**: Business GitHub Account
- **Deployment**: Business Railway Account
- **Standardization**: DO NOT include SSO, central auth, or the Bug Tracker `widget.js`. This is a clean client site.
- **Workflow**: This project is currently "Hands-Off". Only perform critical bug fixes or requested updates.

## Architecture
- **Frontend**: React 19 + Vite + SASS
- **Backend**: Express.js serving static files + API proxy for form submissions
- **No database** — all form data is sent to GoHighLevel webhooks

## Commands
- `npm run dev` — Start Vite dev server
- `npm run build` — Build for production
- `npm start` — Run production server
- `npm run server` — Run server with auto-reload

## Structure
```
server.js           — Express entry point, API routes for form submission
src/
  App.jsx           — Main app with hero section and modal triggers
  components/
    ContactModal    — Quick contact info form
    FinancingForm   — Detailed financing application form
  styles/
    global.scss     — Base styles and .btn class
    _variables.scss — Theme variables (dark theme)
```

## Environment Variables
- `PORT` — Server port (default 3000)
- `GHL_APPLY_WEBHOOK_URL` — GoHighLevel webhook for contact form
- `GHL_FINANCING_WEBHOOK_URL` — GoHighLevel webhook for financing applications
- `VITE_MAIN_SITE_URL` — URL for "Back to Main Site" links

## Deployment
Railway auto-deploys on push to main. See `railway.toml` for config.
