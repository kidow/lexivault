---
name: drill
description: Runs an interactive one-question-at-a-time language drill from the Lexivault Obsidian vault. Use when the user starts a command like /drill 일본어 전체, /drill 일주일 이내 배웠던 것들, /drill 오늘 배운 것, or asks to practice language notes through conversation.
---

# Drill

## Purpose

Run an interactive language drill inside the conversation.

This skill asks one question at a time, waits for the user's answer, checks it, gives concise feedback, and continues.

It does not create Anki cards, does not write generated practice questions into the vault, and does not persist drill history by default.

## Target Vault

`/Users/kidow/Library/Mobile Documents/iCloud~md~obsidian/Documents/lexivault`

## Quick Start

Start a drill with `/drill` plus scope, such as language, time range, or note type.

Examples:

```txt
/drill 일본어 전체
/drill 일주일 이내 배웠던 것들
/drill 일본어 일주일 이내
/drill 독일어 문법
/drill 중국어 단어
/drill 오늘 배운 것
/drill 최근 배운 것
```

## Core Rules

- Interpret `/drill` as a request to start a conversational practice loop.
- Ask exactly one question at a time.
- Do not reveal the answer before the user answers.
- Do not generate a batch of questions.
- Stay grounded in the selected note content.
- Prefer easy questions first unless the user asks for a different level.
- Keep feedback short and specific.

## Scope Parsing

Parse the command into:

1. Language
2. Time range
3. Note type
4. Difficulty
5. Practice mode

## Selection Rules

- Prefer notes with `anki: true`.
- Also allow useful notes with clear recall material even if `anki: false`.
- Use note sections like `Meaning`, `Form`, `Usage`, `Examples`, `Cards`, `Core Idea`, `When To Use`, and `Common Mistakes`.
- Do not rely only on existing `Cards`.
- If a required answer cannot be inferred from the notes, ask a different question.

## Feedback

After each answer, respond with concise correction and the next question.

## New Learning Capture

Only call `capture` when the user explicitly asks to save something, or when the correction reveals a reusable learning item worth preserving.

## Stop Rule

Stop when the user says `그만`, `중단`, `종료`, `stop`, `enough`, or `여기까지`.
