# Drill Reference

## Language Keywords

Map Korean language names to Lexivault folders:

- `영어` -> `01_Languages/English`
- `일본어` -> `01_Languages/Japanese`
- `스페인어` -> `01_Languages/Spanish`
- `포르투갈어` -> `01_Languages/Portuguese`
- `러시아어` -> `01_Languages/Russian`
- `프랑스어` -> `01_Languages/French`
- `독일어` -> `01_Languages/German`
- `아랍어` -> `01_Languages/Arabic`
- `이탈리아어` -> `01_Languages/Italian`
- `중국어` -> `01_Languages/Chinese`

If no language is specified, search across all language folders.

## Type Keywords

Map user-friendly Korean terms to note types:

- `단어`, `어휘`, `vocab`, `vocabulary` -> `Vocabulary`
- `문법`, `grammar` -> `Grammar`
- `문장`, `예문`, `sentences` -> `Sentences`
- `표현`, `회화 표현`, `expressions` -> `Expressions`
- `발음`, `pronunciation` -> `Pronunciation`
- `자료`, `소스`, `sources` -> `Sources`

If no type is specified, include all suitable note types except `Sources` unless the user explicitly asks for source-based review.

## Time Range Keywords

Use `created` and `updated` YAML fields.

- `오늘 배운 것` -> today
- `어제 배운 것` -> yesterday
- `일주일 이내 배웠던 것들` -> last 7 days
- `최근 배운 것` -> last 7 days
- `이번 달` -> current month
- `전체` -> no time filter

If no time range is specified, default to `전체`.

## Question Types

Prefer applied questions over simple memorization:

- translation
- cloze
- sentence completion
- grammar choice
- transformation
- error correction
- short production
- meaning discrimination
- pronunciation or reading check

## Difficulty Adjustment

- Start easy unless the user requests a different level.
- If the user gets two questions wrong in a row, simplify.
- If the user gets three questions right in a row, increase difficulty slightly.
- If the user repeats the same mistake, drill that pattern with simpler examples.

## Feedback Format

After the user answers, use:

```md
판정: 정답 / 부분 정답 / 오답

정답:
...

설명:
...

다음 문제:
...
```

Keep the explanation short. For beginner material, explain in Korean.

## Drill Loop

1. Select one note or one learning point.
2. Ask one question.
3. Wait for the user's answer.
4. Evaluate the answer.
5. Give concise feedback.
6. Ask the next question.

## Stop Summary

When stopping, give a short summary of what was practiced and any recurring mistakes.
