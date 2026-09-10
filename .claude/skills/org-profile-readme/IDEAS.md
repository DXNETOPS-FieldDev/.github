# Org overview page — ideas backlog

Brainstormed while building the current page (2026-09-09). Pick one up, edit `profile/README.md`, check it off here in the same commit.

- [x] **Group projects by category** instead of a flat list — e.g. "App Views", "Grafana Dashboards", "Utilities" — as the repo count grows past ~6 a flat list stops scanning well. **Done:** 2026-09-10 — App Views / Grafana dashboards, under a Public vs Internal split.
- [ ] **Screenshot or GIF per project** — a small thumbnail next to each project (e.g. WeatherMap's map view) sells what it does faster than a one-line description.
- [ ] **Dark/light adaptive logo** — GitHub Markdown supports `#gh-dark-mode-only` / `#gh-light-mode-only` suffixes on image sources so the banner switches with the viewer's theme instead of one fixed PNG.
- [ ] **Tech stack badges** — shields.io badges for Grafana, React, OpenAPI/App View, etc., so visitors see the stack at a glance.
- [x] **"Getting started" blurb** — one or two lines + a link on how someone outside the team would deploy or try one of these App Views. **Done:** 2026-09-10 — "Using these projects" section.
- [x] **Point-of-contact / support line** — who to ping (Slack channel, email) for questions — useful once the org has outside visitors. **Done:** 2026-09-10 — open an issue on the relevant repo (no named POC yet; add one if the team wants).
- [ ] **Auto-refreshed project list via GitHub Action** — a scheduled workflow that regenerates the project list from the GitHub API (name + description) so it can't silently go stale when a repo is renamed or a new one is added.
- [ ] **Turn on Discussions** — surfaced by GitHub's own onboarding panel; could host Q&A instead of issues for cross-project questions.
- [ ] **Social preview image** — set a custom og:image for the org (Settings → social preview) so links shared in Slack/Teams show something branded instead of the default avatar crop.
- [ ] **Roadmap section** — short "what's next" list for visibility into in-progress work (WeatherMap v2, new dashboards, etc.).

- [ ] **Screenshot or GIF per project** — still open, and more valuable now the list is in tables; a thumbnail column would sell each project faster than its sentence.
- [ ] **Auto-refreshed project list via GitHub Action** — more valuable now than when it was first floated: the page carries a **Public vs Internal** split, so a repo whose visibility is flipped silently puts it in the wrong section. A scheduled job could regenerate the list *and* assert each entry's visibility still matches the section it sits in.

## Raised 2026-09-10, needs an owner outside this repo

- [ ] **None of the org's repositories carries a recognized license.** `WeatherMap` and `ThresholdReport` have a `LICENSE` file that GitHub reads as `NOASSERTION`; `grafana-operational-reports`, `grafana-netops-flow-reports` and `Device-Geo-Editor` have **no `LICENSE` at all**, which means default copyright — a customer who clones them has no granted rights. The profile page is written to avoid asserting any usage rights, so it is accurate today, but "public" is currently doing work that only a license can do. **This is an IP decision, not a README change** — it needs whoever owns that at Broadcom.

## Non-README levers (don't require editing this file)

- **Pin repositories** — via the org page UI ("pin repositories"), independent of the README, controls the repo cards shown in the sidebar.
- **Org bio/description/social links** — Settings → Profile, shows under the org name/logo above the README.
