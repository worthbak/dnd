# D&D Session Notes Website - Project Context

## Overview
Building a GitHub Pages site to host D&D campaign session notes across multiple campaigns. Notes are generated from Zoom call transcripts and are in Markdown format. The site is structured to keep campaigns isolated - players from one campaign cannot discover other campaigns.

## Current State
- Repository: `dnd` (public)
- Site structure supports multiple isolated campaigns
- Jekyll-based GitHub Pages site
- Base URL: `https://worthbak.github.io/dnd`

## Repository Structure
```
dnd/
├── _config.yml          # Jekyll config
├── index.md             # Generic landing page (no campaign links)
├── foti/                # Fellowship of the Idiots campaign
│   ├── index.md         # Campaign landing page
│   └── sessions/        # Session notes
│       ├── session-01.md
│       ├── session-02.md
│       └── ...
└── 4burritos/           # Future campaign (example)
    ├── index.md
    └── sessions/
```

## Campaign URLs
- FOTI campaign: `worthbak.github.io/dnd/foti`
- Future campaigns: `worthbak.github.io/dnd/[campaign-name]`
- Generic landing: `worthbak.github.io/dnd` (intentionally has no campaign links)

## Session File Format
Session notes follow this structure:
- Naming: `session-##.md` (e.g., session-01.md, session-17.md)
- Front matter required:
```markdown
---
layout: default
title: Session [X] - [Descriptive Title]
---
```
- Content: Markdown-formatted session notes (bullet points, headers, etc.)

## Adding New Sessions to Existing Campaign
1. Copy session notes from Obsidian vault to appropriate campaign's `/sessions` folder (e.g., `foti/sessions/`)
2. Rename to `session-##.md` format
3. Add Jekyll front matter with appropriate title
4. Update the campaign's `index.md` (e.g., `foti/index.md`) to add link to new session
5. Commit and push to GitHub

## Adding New Campaign
1. Create new campaign folder at root level (e.g., `4burritos/`)
2. Create `index.md` for campaign landing page
3. Create `sessions/` subfolder
4. Add session files following standard format
5. Share specific campaign URL with that group only
6. **Do NOT** add links to new campaign in root `index.md`

## Configuration
`_config.yml` settings:
```yaml
title: D&D Campaign Notes
description: Session notes for active campaigns
theme: jekyll-theme-cayman
baseurl: "/dnd"
```

## Source Files
Original session notes are stored in Obsidian vault at:
`/Users/worthbak/Library/Mobile Documents/iCloud~md~obsidian/Documents/Vault Charlie/Session Notes/`

Each session has its own folder (Session 1/ through Session 16/) containing the original notes. These source files remain untouched - the campaign folders contain formatted copies for the website.

## Security Note
Campaign isolation is maintained by:
- No links between campaigns in any `index.md` files
- No directory listing on GitHub Pages (players can't browse folders)
- Each group only receives their specific campaign URL
