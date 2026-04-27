<p align="center">
  <a href="README.md">English</a> | 
  <a href="README.ko-KR.md">한국어</a>
</p>

# Lexivault

Lexivault is a personal language-learning knowledge base built on an Obsidian vault.

The main workflow is to store structured language-learning knowledge in Obsidian and mark items that need repeated recall for Anki review. As a secondary workflow, the Codex `drill` skill can run AI-assisted conversational quizzes from the vault contents.

## Purpose

- Obsidian: Store language knowledge, examples, grammar, pronunciation, expressions, and sources.
- Anki: Review and memorize material that needs active recall.
- AnkiWeb: Sync Anki across desktop and mobile.
- Codex skills: Assist with capturing learning material and running conversational quizzes.

## Structure

- `00_Inbox/`: Temporary learning material that has not been organized yet.
- `01_Languages/`: Source notes organized by language.
- `02_Review/`: Review queues, Anki candidates, and review logs.
- `03_Templates/`: Note templates.
- `04_Resources/`: Dictionaries, books, external materials, and references.
- `05_Dashboard/`: Study status and review entry points.
- `.codex/skills/`: Codex skills used by this vault.

Under `01_Languages/`, each language usually contains categories such as `Vocabulary`, `Grammar`, `Sentences`, `Expressions`, `Pronunciation`, and `Sources`.

## Main Workflows

### 1. Capture

The `capture` skill stores newly learned language material in the correct language and category folder.

It generally does the following:

- Classifies input as vocabulary, grammar, sentences, expressions, pronunciation, or sources.
- Detects the language, and for Chinese also distinguishes variety and script variant.
- Reads likely existing target notes before editing when duplicates are possible.
- Creates or updates notes with matching YAML frontmatter and body structure.
- Marks only material worth active recall as `anki: true`.

If the language, note type, Chinese variant, or duplicate merge decision is unclear, the skill asks a question before writing.

### 2. Anki Review

Anki is used for minimal units of repeated recall, not for memorizing entire Obsidian notes as-is.

Recommended flow:

1. Write and organize learning material in Obsidian first.
2. Mark only review-worthy items as `anki: true`.
3. Manage card candidates through `02_Review/Anki_Candidates/` or related review documents.
4. Keep Anki cards simple and explicit, usually in a question-and-answer shape.

### 3. Drill

The `drill` skill runs conversational quizzes from the vault contents.

- It asks one question at a time.
- It waits for the user's answer.
- It gives concise correction and moves to the next question.
- By default, it does not create Anki cards or persist drill history in the vault.

Examples:

```text
/drill Japanese all
/drill what I learned today
/drill things learned within the last week
```

## Daily Use

1. Capture newly learned material quickly.
2. Use the `capture` skill to move it into the right language and note type.
3. Start review from `05_Dashboard/Study Dashboard.md`.
4. Manage memorization targets as Anki candidates.
5. Use the `drill` skill when you want a conversational check.

## References

- [Obsidian Anki Guide.md](Obsidian%20Anki%20Guide.md): Operating rules for using Obsidian and Anki together
- [.codex/skills/capture/SKILL.md](.codex/skills/capture/SKILL.md): Learning-material capture skill
- [.codex/skills/drill/SKILL.md](.codex/skills/drill/SKILL.md): Conversational quiz skill
