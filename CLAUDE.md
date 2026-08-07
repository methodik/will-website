# Project Instructions

## Development workflow (feature branches)

Every feature request from the user MUST follow this process:

1. **Branch**: Create a new branch off `main` named `feature/<short-description>` (e.g. `feature/contact-form`).
2. **Build**: Implement the feature on that branch, committing as you go.
3. **Verify**: Confirm the feature works (browser preview for anything visual).
4. **Merge**: When the feature is complete and verified, merge the branch back into `main` and delete the feature branch.

## Deployment rules

- **NEVER deploy to a live website without the user's explicit permission in the current conversation.** Merging to `main` locally is allowed as part of the normal workflow; deploying is not. Permission is per-deploy — one approval does not cover future deploys.
- **Hosting**: GitHub Pages, serving the root of `main` from https://github.com/methodik/will-website. Live URL: https://methodik.github.io/will-website/
- **Pushing `main` to GitHub IS the deploy** — Pages republishes automatically on every push to `main`. Therefore: merge features into local `main` freely, but do NOT `git push` main until the user explicitly approves a deploy. Feature branches may be pushed to GitHub at any time (they don't publish anything).

## Release logging (Notion)

Every time a deploy to the live website happens, create ONE new entry in the Notion "Releases" database:

- Page: "Will" — https://app.notion.com/p/matnicole/Will-3b5b77aa1f878041a2bde901e272723c
- Data source ID: `collection://3b5b77aa-1f87-80aa-80d0-000ba59bff63`
- Columns to fill in:
  - **Release** (title): short release name, e.g. "v3 — Contact form + nav fixes"
  - **Deploy Date** (date): the date of the deploy
  - **Features Included** (text): plain-English list of what shipped
  - **Branch(es) Merged** (text): the feature branch names included in this deploy
  - **Commit / Tag** (text): the `main` commit hash (short) deployed
  - **Status** (select): `Deployed` (use `Rolled Back` if a deploy is reverted, `Planned` for a queued release)
  - **Notes** (text): anything noteworthy — issues, follow-ups, context

Log entries are created via the Notion MCP (`notion-create-pages` with the data source ID above). Only log when an actual deploy happens — not on merges to `main`.
