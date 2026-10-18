# PackComply V12 — clean Vercel deployment

Upload these files to the ROOT of the GitHub repository.

## Structure
- index.html — main Free Compliance Checker
- ai-inspector.html — separate AI Packaging Inspector page
- api/inspect.js — Vercel serverless AI endpoint
- data.json — product/country data
- rules.json — preliminary rule library
- package.json
- vercel.json
- .env.example

## Vercel
Framework Preset: Other
Root Directory: ./
Build Command: leave OFF / None
Output Directory: leave OFF / None
Install Command: npm install (or leave default)

## AI
Add OPENAI_API_KEY as a Vercel Environment Variable if live AI inspection is required. Without the key, the AI page returns a clearly labelled demo result instead of failing.

## Important
The Free Check is browser-side and does not call the AI function. The AI page is separate and calls /api/inspect only after an image is uploaded.
