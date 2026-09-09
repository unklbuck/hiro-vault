---
title: "Conversation – Obsidian Vault Export Skill"
date: 2026-09-08
type: conversation-export
aliases: [obsidian vault export skill]
tags: [export, conversation, skills, obsidian]
characters: []
project: Grok Skills
source: grok-session
status: exported
---

# Obsidian Vault Export Skill

> [!summary]
> Built the `obsidian-vault-export` skill and immediately used it to export this same session as an Obsidian-ready note.

## Key Outcomes
- New skill lives at `/home/workdir/.grok/skills/obsidian-vault-export/`
- Skill validated with `validate-skill.sh` (162 lines in SKILL.md)
- Staging root is `/home/workdir/artifacts/obsidian-export/`
- Export types — `conversation`, `image`, `bundle`
- Delivery is workspace file plus optional zip download or GitHub push
- This environment cannot write into a desktop or phone Obsidian folder

## Decisions
- Default GitHub repo — `unklbuck/hiro-vault`
- Preferred when reachable — `unklbuck/hiro-obsidian-vault`
- Suggested vault landing — `inbox/` first, then `archives/conversations/` or `archives/image-sessions/`
- Conversation exports summarize by default — no full transcript unless asked
- Images copy into a sibling `attachments/` folder, never inline base64
- Complements existing skills rather than replacing them — `image-session-archiver`, `github-conversation-archiver`, `github-workflow-automator`

## Characters and Links
- [[obsidian-vault-export]]
- [[hiro-vault]]
- [[hiro-obsidian-vault]]
- Related skills — [[github-workflow-automator]], [[image-session-archiver]], [[github-conversation-archiver]]

## Selected Notes
- Trigger phrases — export to Obsidian, save to my local vault, drop this into Obsidian, export this conversation, export this image
- Script — `scripts/export-to-obsidian.sh`
- Templates — `assets/conversation-note.md`, `assets/image-note.md`, `assets/bundle-note.md`
- References — `references/script-usage.md`, `references/vault-paths.md`, `references/obsidian-formatting.md`

## Next Actions
- If Obsidian Git is pointed at this repo, pull to pick up `archives/conversations/`
- Optional — run an image or bundle export on the next generation session
