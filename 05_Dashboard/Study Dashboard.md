# Study Dashboard

## Quick Links

- [[Language Learning Architecture]]

## Review Queue

```dataview
TABLE language, type, level, source, status, anki
FROM "01_Languages"
WHERE status = "draft" OR status = "learning" OR status = "active" OR anki = true
SORT status ASC, file.mtime DESC
```

## Anki Candidates

```dataview
TABLE language, type, level, source, file.link
FROM "01_Languages"
WHERE anki = true
SORT file.mtime DESC
```

## Language Coverage

```dataview
TABLE
  length(rows) AS notes
FROM "01_Languages"
GROUP BY language
SORT language ASC
```

## By Type

```dataview
TABLE
  length(rows) AS notes
FROM "01_Languages"
GROUP BY type
SORT type ASC
```

## Recently Updated

```dataview
TABLE language, type, status, file.mtime AS updated
FROM "01_Languages"
SORT file.mtime DESC
LIMIT 20
```
