# dottracks.app — DotTracks Marketing & Legal Website

The public-facing site for the DotTracks Android puzzle game.

## Pages

- `/`            — Landing page
- `/privacy`     — Privacy Policy (GDPR + FADP + CCPA compliant)
- `/impressum`   — Impressum (Swiss UWG)
- `/tos`         — Terms of Service (placeholder; full version comes
                   with Premium IAP launch)

## Tech

Plain static HTML + CSS. Zero dependencies, zero build step.

## Deploy

Works on any static host. Recommended:

1. **Vercel** — `vercel --prod` (uses `vercel.json` for clean URLs)
2. **Cloudflare Pages** — connect this repo, set build command empty,
   output directory `.`
3. **GitHub Pages** — push to `main`, enable Pages from repo settings

Custom domain `dottracks.app` should point to whichever host you choose.

## Updating the Privacy Policy

The text in `/privacy/index.html` is mirrored from the in-app version
in `C:\dev\trainyard2.0\src\trainyard.jsx` (`PRIVACY_POLICY_TEXT`).
When either side changes, update both to keep them byte-identical.
