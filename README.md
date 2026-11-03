# FestiveList

Family Christmas Wishlist — shareable between users.

## How sharing works

1. Open the app and add yourself / your gifts as normal.
2. Tap the share button. This automatically creates a unique **family code** and puts it in the URL (e.g. `?family=x7k9p2`).
3. Send that link to family members.
4. Anyone who opens the same link sees and can edit the **same shared list**.

Data is stored permanently on Netlify Blobs (server-side). A local backup is also kept in the browser.

## Deploying

1. Connect this repo to Netlify.
2. Netlify will automatically install `@netlify/blobs` and deploy the function.
3. The site + `/api/family` endpoint will be live.

## Local development

```bash
npm install
npx netlify dev
```

## Project structure

- `index.html` — the app (frontend)
- `netlify/functions/family.js` — API for loading/saving shared family lists
- `netlify.toml` — Netlify config
