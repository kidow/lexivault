---
name: translate
description: Translates a given phrase into English, Japanese, Simplified Chinese, Traditional Chinese, Spanish, French, German, Portuguese, Italian, and Arabic. Use when the user asks to translate text into multiple languages or wants a parallel multilingual translation output.
---

# Translate

## Purpose

Translate the user's phrase into these languages in this order:

1. English
2. Japanese
3. Chinese (Simplified)
4. Chinese (Traditional)
5. Spanish
6. French
7. German
8. Portuguese
9. Italian
10. Arabic

## Output Format

- Use separate section headings for each language.
- Keep the translations aligned to the same source meaning.
- Preserve names, numbers, code, and product terms unless translation would be natural and unambiguous.
- If the source phrase is ambiguous, choose the most likely reading and keep the output natural.

## Workflow

1. Read the user's phrase.
2. Infer the source meaning from context if needed.
3. Translate into each target language.
4. Return only the translations unless the user asks for notes or alternatives.

## Stop And Ask

Ask one concise question before translating if:

- The source phrase is missing.
- The intended meaning is too ambiguous to translate safely.
- The user wants a special register, tone, or audience and did not specify it.
