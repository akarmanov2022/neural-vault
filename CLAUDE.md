# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is an Obsidian vault organized as a Zettelkasten — a personal knowledge management system. Notes are written in Russian. There is no build system, test suite, or application code; the "codebase" is a collection of Markdown notes with YAML frontmatter.

## Note naming convention

All notes follow the pattern: `YYYYMMDDHHmm – <Title>.md`

The timestamp prefix is generated automatically by the Templater plugin. When creating notes manually, match this format exactly.

## Frontmatter schema

Every note has YAML frontmatter. Fields vary by note type:

**zettel** (atomic idea note):
```yaml
id: YYYYMMDDHHmmss
type: zettel
tags: []
aliases: []
source:
created: YYYY-MM-DD
updated: YYYY-MM-DD
```

**literature** (book/article notes):
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

**list**:
```yaml
id: YYYYMMDDHHmmss
type: list
tags: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
```

## Structure conventions

- Each note ends with a `## Связана с` (Related to) section for wiki-style links to other notes.
- Attachments go in `attachments/`.
- Templates live in `templates/` and are excluded from Obsidian's file index (`userIgnoreFilters`).
- `templates/` and `attachments/` are also excluded from Obsidian search.

## Git workflow

Backups are managed by the **obsidian-git** plugin with commit message format: `vault backup: YYYY-MM-DD HH:mm:ss`. Manual commits should follow the same format.

## Installed plugins (relevant to note structure)

- **Templater** — powers all templates in `templates/`; use `zettel-template`, `literature-template`, `project-template`, or `list-template`
- **QuickAdd** — macro-based note creation
- **obsidian-git** — auto-backup to this git repo
- **Zotero Desktop Connector** — literature notes may be linked to Zotero entries via `source:` field
