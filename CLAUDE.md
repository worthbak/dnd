Here's a context document for Claude Code:

---

# D&D Session Notes Website - Project Context

## Overview
Building a GitHub Pages site to host D&D campaign session notes. Notes are generated from Zoom call transcripts and are in Markdown format.

## Current State
- Repository created: `worthbak.github.io` (public)
- Repository cloned locally
- `_config.yml` created with basic Jekyll configuration
- `index.md` created as landing page
- `/sessions` folder created (empty, ready for markdown files)

## What's Needed
1. Session note markdown files need to be added to `/sessions` folder
2. Each session file should have Jekyll front matter at the top:
```markdown
---
layout: default
title: Session [X] - [Title]
---
```
3. `index.md` needs to be updated to link to all session files
4. Optional: improve navigation/structure if there are many sessions
5. Push everything to GitHub to go live at `https://worthbak.github.io`

## File Structure
```
worthbak.github.io/
├── _config.yml          # Jekyll config (already created)
├── index.md             # Landing page (already created)
└── sessions/            # Session notes go here (folder created)
    ├── session-01.md
    ├── session-02.md
    └── ...
```

## Session Notes
All session notes are in Markdown format and ready to be added to the `/sessions` folder.
