# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is an Obsidian vault organized as a Zettelkasten — a personal knowledge management system. Notes are written in Russian. There is no build system, test suite, or application code; the "codebase" is a collection of Markdown notes with YAML frontmatter.

## Note naming convention

All notes follow the pattern: `YYYYMMDDHHmm – <Title>.md`

The timestamp prefix is generated automatically by the Templater plugin. When creating notes manually, match this format exactly.

## Note types and workflow

Three-level workflow based on "How to Take Smart Notes":
1. **Quick capture** → `inbox.md` (one bullet per thought via QuickAdd "⚡ Быстрая мысль")
2. **Literature notes** (`type: literature`) — notes while reading, own words, with source
3. **Permanent notes** (`type: zettel`) — atomic ideas, must have ≥1 link in "Связана с"

Navigation hubs are `MOC — *.md` files (`type: moc`) — one per topic cluster.

## Frontmatter schema

**zettel** (atomic idea):
```yaml
id: YYYYMMDDHHmmss
type: zettel
tags: []
aliases: []
source:
processed_from:
created: YYYY-MM-DD
updated: YYYY-MM-DD
```

**literature** (book/article):
```yaml
id: YYYYMMDDHHmmss
type: literature
tags: [литература]
source: ""
created: YYYY-MM-DD
updated: YYYY-MM-DD
```

**project**:
```yaml
id: YYYYMMDDHHmmss
type: project
tags: [проект]
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
```

**list**, **fleeting**, **daily**, **moc** — same pattern with corresponding `type:` value.

## Structure conventions

- Each note ends with `## Связана с` for wiki-style links. Every zettel must have ≥1 link here.
- Attachments go in `attachments/`.
- Templates live in `templates/` (excluded from Obsidian's file index).
- Daily notes go in `daily-notes/` (format: `YYYY-MM-DD.md`).
- `inbox.md` — persistent quick-capture target; process daily, delete processed lines.

## Hotkeys (Mac)

- `Cmd+Shift+F` — quick capture to inbox.md
- `Cmd+N` — new zettel (via Templater)
- `Cmd+Shift+S` — git push

## Git workflow

Auto-commit every 5 min, auto-push/pull every 10 min via obsidian-git. On iPhone: push manually before closing the app (Git ribbon → Push). Commit message format: `vault backup: YYYY-MM-DD HH:mm:ss`.

## Installed plugins (relevant to note structure)

- **Templater** — powers all templates in `templates/`
- **QuickAdd** — 5 commands: ⚡ Быстрая мысль (capture), ✏️ Новый Zettel, 📚 Литературная заметка, 🚀 Новый проект, 📋 Новый список
- **obsidian-git** — auto-backup and sync Mac ↔ iPhone
- **Zotero Desktop Connector** — literature notes linked via `source:` field
