# Add Language Note Reference

## Classification

- `Vocabulary`: one word, lexical item, fixed collocation, or idiom-like item.
- `Grammar`: one grammar concept, conjugation pattern, particle, tense, agreement rule, or construction.
- `Sentences`: date/source-based sentence collections or batches of practice examples.
- `Expressions`: reusable phrase, set expression, pragmatic formula, or conversational pattern.
- `Pronunciation`: sound system, accent, phonetics, spelling-to-sound, tones, pitch, or reading rules.
- `Sources`: books, lessons, videos, dictionaries, apps, and source-centered notes.

If one input contains multiple unrelated items, create separate notes unless the user asks for a collection.

## Folder Mapping

- English: `01_Languages/English/{Vocabulary,Grammar,Sentences,Expressions,Pronunciation,Sources}`
- Japanese: `01_Languages/Japanese/{Vocabulary,Grammar,Sentences,Expressions,Pronunciation,Sources}`
- Spanish: `01_Languages/Spanish/{Vocabulary,Grammar,Sentences,Expressions,Pronunciation,Sources}`
- Portuguese: `01_Languages/Portuguese/{Vocabulary,Grammar,Sentences,Expressions,Pronunciation,Sources}`
- Russian: `01_Languages/Russian/{Vocabulary,Grammar,Sentences,Expressions,Pronunciation,Sources}`
- French: `01_Languages/French/{Vocabulary,Grammar,Sentences,Expressions,Pronunciation,Sources}`
- German: `01_Languages/German/{Vocabulary,Grammar,Sentences,Expressions,Pronunciation,Sources}`
- Arabic: `01_Languages/Arabic/{Vocabulary,Grammar,Sentences,Expressions,Pronunciation,Sources}`
- Italian: `01_Languages/Italian/{Vocabulary,Grammar,Sentences,Expressions,Pronunciation,Sources}`

Chinese:

- Mandarin shared material: `01_Languages/Chinese/Mandarin/Common/{Grammar,Pronunciation,Resources}`
- Mandarin simplified: `01_Languages/Chinese/Mandarin/Simplified/{Vocabulary,Sentences,Expressions,Sources}`
- Mandarin traditional: `01_Languages/Chinese/Mandarin/Traditional/{Vocabulary,Sentences,Expressions,Sources}`
- Cantonese shared material: `01_Languages/Chinese/Cantonese/Common/{Grammar,Pronunciation,Resources}`
- Cantonese traditional: `01_Languages/Chinese/Cantonese/Traditional/{Vocabulary,Sentences,Expressions,Sources}`

## YAML

Every note starts with:

```yaml
---
language:
type:
level:
source:
status: draft
anki: false
created:
updated:
meaning_ko:
---
```

Set `created` and `updated` to the current local date in `YYYY-MM-DD`.

Chinese fields:

```yaml
variety:
script_variant:
script_simplified:
script_traditional:
pinyin:
jyutping:
tone:
measure_word:
```

Japanese fields:

```yaml
kanji:
kana:
romaji:
pitch_accent:
jlpt_level:
```

Arabic fields:

```yaml
arabic:
transliteration:
root:
pattern:
diacritics:
rtl: true
```

## Body Templates

Vocabulary sections: `Meaning`, `Form`, `Usage`, `Examples`, `Related`, `Cards`.

Grammar sections: `Core Idea`, `Form`, `When To Use`, `Examples`, `Common Mistakes`, `Related`, `Cards`.

Expression sections: `Meaning`, `Register`, `Usage`, `Examples`, `Related`, `Cards`.

Sentence collection sections: `Sentences`, `Card Candidates`.

## Anki Policy

Keep `anki: false` unless the note contains clear recall material. Use `anki: true` for vocabulary, core grammar rules, high-value expressions, minimal pairs, tones, conjugations, and sentence patterns that the user should actively recall.

Add concise card candidates:

```md
- Q:
  A:
```

## File Naming

Use readable filenames. Prefer the target-language item for vocabulary and expressions. Use concise English or Korean titles for grammar concepts when the original script would be awkward.

Avoid overwriting. If a matching note exists, update it instead of creating a duplicate.
