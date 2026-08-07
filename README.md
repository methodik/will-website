# Nausta — Homepage

Single-page marketing site for Nausta, a UK accounting firm (working name). One
self-contained HTML file, vanilla HTML/CSS/JS, no build step. Built from the
Claude Design handoff (`Homepage design directions.zip`) — the design brief and
approved prototypes are the source of truth for layout, copy and tokens.

All bracketed values like `[Name]`, `[COMPANY]` and `+44 7XXX XXX XXX` are
deliberate placeholders awaiting client content. The contact form posts to a
placeholder endpoint (see the TODO comment in `index.html`).

## Running locally

Open `index.html` in a browser, or serve it with:

```bash
npx serve . -l 8901
```

Then visit http://localhost:8901.
