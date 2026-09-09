---
name: org-profile-readme
description: Edit the DXNETOPS-FieldDev GitHub org overview page (github.com/DXNETOPS-FieldDev) — the README, logo/banner, and project list rendered above the repo grid. Use whenever someone wants to change what shows on the org's public overview page, add/remove a project from the list, swap the logo, or add images/badges to it.
---

# DXNETOPS-FieldDev org profile README

## The mechanism (easy to get wrong)

GitHub renders the org overview page from **one specific file**:

```
DXNETOPS-FieldDev/.github repo → profile/README.md   (repo must be PUBLIC)
```

This repo (the one this skill lives in) *is* that `.github` repo — you're already in the right place.

**Common wrong guess:** creating a repo literally named `DXNETOPS-FieldDev` (matching the org login) and putting a README at its root. That was the old GitHub mechanism and no longer works — GitHub now silently ignores it. Don't recreate that repo; it was tried and removed on 2026-09-09.

## Layout in this repo

```
profile/
  README.md              ← rendered content, top of https://github.com/DXNETOPS-FieldDev
  images/
    broadcom-logo.png     ← banner logo, referenced via relative path
```

Images embed with normal Markdown, relative to `profile/`:
```markdown
![alt text](images/broadcom-logo.png)
```
Any file type can be *committed* here, but only what the Markdown renderer supports (images, tables, badges, collapsible `<details>`, limited sanitized HTML) actually displays inline. PDFs/videos need an external host or a `user-attachments` asset link — they don't preview from a repo-relative path.

## Workflow to change it

```bash
git pull
# edit profile/README.md or add files under profile/images/
git add profile/README.md profile/images/<file>
git commit -m "..."
git push
```

Changes typically show up on the org page within a few minutes (occasionally longer — GitHub caches the rendered org page).

## Verifying it actually rendered

The org page looks different logged-in (as an org member) vs logged-out (public). As a member you'll see an onboarding/dashboard panel ("We think you're gonna like it here...") instead of the README by default — use the **"View as: Public"** dropdown in the sidebar to see what visitors actually see, or just check logged-out:

```bash
curl -s -A "Mozilla/5.0" "https://github.com/DXNETOPS-FieldDev" | grep -o 'markdown-body[^"]*'
```
If that returns `markdown-body entry-content container-lg f5`, the README is rendering. Don't rely on grepping for phrases that also appear in repo card descriptions on the sidebar — that produces false positives (learned this the hard way: repo descriptions duplicated text from the README and made an unrendered README look rendered).

## Dismissing the "getting started" onboarding panel

That panel is a personal, member-only UI element — not something in this repo. Each member dismisses it individually via **"hide the tasks we've suggested"** in the sidebar of their own logged-in view.

## Ideas backlog

See [IDEAS.md](IDEAS.md) for enhancement ideas floated for this page — pick one up, discuss with the other collaborator, check it off.
