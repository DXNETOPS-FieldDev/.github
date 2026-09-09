# DXNETOPS-FieldDev/.github

This is the org's special `.github` repository. GitHub uses it for two things:

1. **Org profile README** — [`profile/README.md`](profile/README.md) is rendered at the top of **[github.com/DXNETOPS-FieldDev](https://github.com/DXNETOPS-FieldDev)**, above the repo grid. That's what visitors see when they land on the org.
2. **Org-wide defaults** (issue templates, contributing guide, etc.) — none set up yet, but this is the repo where they'd go.

This file (the root `README.md`) is just documentation for people working in this repo — it does not appear on the org page.

## Clone

```bash
git clone https://github.com/DXNETOPS-FieldDev/.github.git
```

## Making a change to the org overview page

Don't hand-edit blind — read the skill first:

```
.claude/skills/org-profile-readme/SKILL.md   ← how the mechanism works, gotchas, verification steps
.claude/skills/org-profile-readme/IDEAS.md   ← backlog of enhancement ideas, pick one up
```

If you're using Claude Code, it picks up that skill automatically once you're in this repo — just ask it to change the org overview page.

Quick version: edit [`profile/README.md`](profile/README.md) (images go in `profile/images/`), commit, push to `main`. Changes to the public org page usually show up within a few minutes.
