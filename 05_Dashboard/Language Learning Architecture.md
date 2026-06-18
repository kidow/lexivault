# Language Learning Architecture

## Principles

- Obsidian is the source of truth for language knowledge.
- Anki is optional, but notes should be structured so they can become Anki cards later.
- Folder structure is shared across languages where possible.
- Language-specific needs are handled with extra YAML fields, not completely different note shapes.

## Top-Level Structure

```text
00_Inbox/
01_Languages/
02_Review/
03_Templates/
04_Resources/
05_Dashboard/
```

## Note Types

```text
Vocabulary  = one word or lexical item
Grammar     = one grammar concept
Sentences   = date/source-based sentence collections
Expressions = one reusable phrase or expression
Pronunciation = sound system, accent, phonetics
Sources     = books, videos, apps, lessons, dictionaries
```

## Chinese Structure

Chinese is organized by variety first, then script or common material.

```text
Chinese/
  Mandarin/
    Common/
      Grammar/
      Pronunciation/
      Resources/
    Simplified/
      Vocabulary/
      Sentences/
      Expressions/
      Sources/
    Traditional/
      Vocabulary/
      Sentences/
      Expressions/
      Sources/
  Cantonese/
    Common/
      Grammar/
      Pronunciation/
      Resources/
    Traditional/
      Vocabulary/
      Sentences/
      Expressions/
      Sources/
```

## Common YAML Fields

```yaml
language:
type: vocabulary | grammar | sentence | expression | pronunciation | source
level:
source:
status: draft | learning | active | mastered | archived
anki: false
created:
updated:
```

## Language-Specific Fields

### Chinese

```yaml
language: Chinese
variety: Mandarin
script_variant: Simplified
script_simplified:
script_traditional:
pinyin:
jyutping:
tone:
measure_word:
meaning_ko:
transliteration_ko:
```

### Japanese

```yaml
language: Japanese
kanji:
kana:
romaji:
pitch_accent:
jlpt_level:
meaning_ko:
transliteration_ko:
```

### Arabic

```yaml
language: Arabic
arabic:
transliteration:
root:
pattern:
diacritics:
rtl: true
meaning_ko:
transliteration_ko:
```

## Anki Policy

- Keep `anki: false` by default.
- Change to `anki: true` only when a note has clear recall value.
- Prefer card candidates in the `## Cards` section.
- Do not turn every note into a card.
