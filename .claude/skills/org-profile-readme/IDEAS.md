# Org overview page — ideas backlog

Brainstormed while building the current page (2026-09-09). Pick one up, edit `profile/README.md`, check it off here in the same commit.

- [ ] **Group projects by category** instead of a flat list — e.g. "App Views", "Grafana Dashboards", "Utilities" — as the repo count grows past ~6 a flat list stops scanning well.
- [ ] **Screenshot or GIF per project** — a small thumbnail next to each project (e.g. WeatherMap's map view) sells what it does faster than a one-line description.
- [ ] **Dark/light adaptive logo** — GitHub Markdown supports `#gh-dark-mode-only` / `#gh-light-mode-only` suffixes on image sources so the banner switches with the viewer's theme instead of one fixed PNG.
- [ ] **Tech stack badges** — shields.io badges for Grafana, React, OpenAPI/App View, etc., so visitors see the stack at a glance.
- [ ] **"Getting started" blurb** — one or two lines + a link on how someone outside the team would deploy or try one of these App Views.
- [ ] **Point-of-contact / support line** — who to ping (Slack channel, email) for questions — useful once the org has outside visitors.
- [ ] **Auto-refreshed project list via GitHub Action** — a scheduled workflow that regenerates the project list from the GitHub API (name + description) so it can't silently go stale when a repo is renamed or a new one is added.
- [ ] **Turn on Discussions** — surfaced by GitHub's own onboarding panel; could host Q&A instead of issues for cross-project questions.
- [ ] **Social preview image** — set a custom og:image for the org (Settings → social preview) so links shared in Slack/Teams show something branded instead of the default avatar crop.
- [ ] **Roadmap section** — short "what's next" list for visibility into in-progress work (WeatherMap v2, new dashboards, etc.).

## Non-README levers (don't require editing this file)

- **Pin repositories** — via the org page UI ("pin repositories"), independent of the README, controls the repo cards shown in the sidebar.
- **Org bio/description/social links** — Settings → Profile, shows under the org name/logo above the README.
