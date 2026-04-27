---
name: capture
description: Captures foreign-language learning material into the Lexivault Obsidian vault with the correct folder, YAML fields, note structure, and Anki readiness. Use when the user asks to add, record, save, organize, or turn learned language content into Obsidian notes for English, Japanese, Chinese, Spanish, Portuguese, Russian, French, German, Arabic, or Italian.
---

# Capture

## Target

Vault:

`/Users/kidow/Library/Mobile Documents/iCloud~md~obsidian/Documents/lexivault`

Use this skill when the user gives language-learning material and expects Codex to create or update Obsidian notes in that vault.

## Workflow

1. Classify the input as `Vocabulary`, `Grammar`, `Sentences`, `Expressions`, `Pronunciation`, or `Sources`.
2. Determine language, and for Chinese determine `variety` and `script_variant`.
3. Read any existing likely target note before editing.
4. Create or update the note with YAML frontmatter and a matching body structure.
5. Mark `anki: true` only for material worth active recall.
6. Verify the created or updated file exists.
7. Reply in Korean with paths, non-obvious classification decisions, blanks left for the user, and a suggested commit message.

## Stop And Ask

Ask one concise question before writing if:

- The language is unclear.
- The note type is unclear.
- Chinese variety or script is unclear.
- The target note may duplicate an existing note and merging would be risky.
- Required content is too vague to make a useful note.

## Reference

Read [REFERENCE.md](REFERENCE.md) when creating or updating notes. It contains folder mappings, YAML fields, body templates, Anki policy, and file naming rules.
