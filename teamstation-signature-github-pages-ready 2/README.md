# TeamStation AI Email Signatures

Static GitHub Pages package for the TeamStation AI email signature studio.

## What is included

- `index.html` — team-facing signature studio with presets, editable fields, live preview, and copy buttons.
- `dist/lonnie.html` — Lonnie McRorey's ready-made signature page.
- `templates/teamstation-signature-template.html` — reusable table-based HTML fragment with placeholders.
- `assets/teamstation-logo-160.png` — production logo image for email signatures.
- `assets/teamstation-logo-96.png` — smaller logo asset.
- `assets/teamstation-logo-source.png` — original source logo.
- `.nojekyll` — tells GitHub Pages to serve files directly.

## Push this package to GitHub

From this folder:

```bash
git init
git add .
git commit -m "Add TeamStation AI email signature site"
git branch -M main
git remote add origin https://github.com/TeamStationAIAxiomVertex/signature.git
git push -u origin main
```

If `origin` already exists, use:

```bash
git remote set-url origin https://github.com/TeamStationAIAxiomVertex/signature.git
git push -u origin main
```

## Enable GitHub Pages

In the GitHub repository:

1. Go to **Settings** → **Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Set **Branch** to `main` and folder to `/root`.
4. Save.

After the Pages deployment completes, the team page should be available at:

```text
https://teamstationaiaxiomvertex.github.io/signature/
```

Lonnie's direct signature page should be available at:

```text
https://teamstationaiaxiomvertex.github.io/signature/teamstation-signature-github-pages-ready%202/dist/lonnie.html
```

The logo URL used inside the email signatures is:

```text
https://teamstationaiaxiomvertex.github.io/signature/teamstation-signature-github-pages-ready%202/assets/teamstation-logo-160.png
```

## Team install workflow

1. Open the GitHub Pages URL: `https://teamstationaiaxiomvertex.github.io/signature/`.
2. Choose a preset or enter the team member's name, title, email, phone, calendar URL, and optional links.
3. Click **Copy signature** to copy the rendered rich signature.
4. Paste into Gmail, Outlook, Apple Mail, or another rich text signature editor.
5. Send a test email to confirm the logo renders and every link opens correctly.

For Gmail, paste the rendered signature into **Settings** → **See all settings** → **General** → **Signature**. Do not paste raw HTML into Gmail's signature box.

For Outlook, paste the rendered signature into **Settings** → **Accounts** → **Signatures**.

## Important implementation note

Email clients require the logo to be publicly reachable by absolute URL. This package uses conservative table markup, inline styles, fixed logo dimensions, and GitHub Pages for the public logo URL. If TeamStation later hosts the logo at a branded domain, update all instances of:

```text
https://teamstationaiaxiomvertex.github.io/signature/teamstation-signature-github-pages-ready%202/assets/teamstation-logo-160.png
```

to the branded URL, for example:

```text
https://brand.teamstation.dev/signatures/teamstation-logo-160.png
```
