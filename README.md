# LCP Assistant — PWA Chat App

AI-powered chatbot for Leftfield Capital Partners. Connected to Monday.com in real time. Installable as an app on iPhone, Android, and desktop.

## What it does

- Ask about the deal pipeline, portfolio, BBSW rates, maturity dates
- Update deal stages and add notes directly from chat
- Works on any device — install it as an app on your phone

## Setup (10 minutes)

### 1. Add app icons

Create a folder `public/icons/` and add two PNG files:
- `icon-192.png` — 192×192px, navy background (#0d1e2c), LCP logo in teal
- `icon-512.png` — 512×512px, same design

You can create these in Canva using LCP brand colours.

### 2. Push to GitHub

```bash
git init
git add .
git commit -m "LCP Assistant PWA"
git remote add origin https://github.com/YOUR_USERNAME/lcp-chat-app
git push -u origin main
```

### 3. Deploy to Vercel

1. Go to vercel.com/new
2. Import your GitHub repo
3. Click Deploy

### 4. Add environment variables

In Vercel → your project → Settings → Environment Variables:

| Name | Value | Where to get it |
|------|-------|-----------------|
| `ANTHROPIC_API_KEY` | `sk-ant-...` | console.anthropic.com |
| `MONDAY_API_TOKEN` | `eyJ...` | monday.com → Profile → Developers → API |

Then redeploy: Vercel → Deployments → Redeploy.

### 5. Install on your phone

**iPhone:**
1. Open your Vercel URL in Safari
2. Tap the Share button
3. Tap "Add to Home Screen"
4. Tap Add

**Android:**
1. Open your Vercel URL in Chrome
2. Tap the menu (three dots)
3. Tap "Add to Home Screen"

## Tech stack

- Plain HTML/CSS/JS — no framework needed
- Vercel serverless function for the API
- Claude claude-sonnet-4-20250514 with Monday.com MCP
- PWA with service worker for installability

## Sharing with the team

Once deployed, share the Vercel URL with Malcolm, Dino, and anyone else at LCP. They can install it on their own phones the same way.
