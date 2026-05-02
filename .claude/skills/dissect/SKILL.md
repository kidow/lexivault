---
name: dissect
description: Deep-reads a long foreign-language text (article, song lyrics, novel excerpt, etc.) pasted into the session. Claude auto-detects the text type, breaks it into meaningful sections, and guides the user through language + context analysis. Use when the user runs /dissect and pastes a text.
---

# Dissect

## Purpose

Take a pasted foreign-language text and systematically take it apart — language, meaning, cultural context, authorial intent — section by section.

Not a translator. Not a vocabulary list. A guided deep reading.

## Trigger

User runs `/dissect` and pastes the full text (or pastes text first, then calls `/dissect`).

## Step 1: Auto-detect Text Type

Identify the text type from content and structure:

| Type | Cues | Section unit |
|------|------|--------------|
| 노래 가사 | 반복 구절, 짧은 행, 운율 | Verse / Chorus / Bridge |
| 뉴스·아티클 | 단락 구조, 사실 중심 | 논점 단위 (도입 / 본론 / 결론) |
| 소설·산문 | 서술·대화 혼합, 장면 전환 | 장면 단위 |
| 에세이·칼럼 | 주장 + 근거 반복 | 주장 단위 |
| 기타 | 판단 불가 시 문단 단위 |

텍스트 유형을 한 줄로 밝히고 분석 시작.

## Step 2: 오프닝 — 흥미로운 포인트 3가지

전체를 먼저 읽고, 이 글에서 파고들 만한 포인트 3가지를 제시.

형식:
> 이 [유형]에서 주목할 만한 포인트:
> 1. [언어적 특징 or 표현]
> 2. [맥락/배경 지식]
> 3. [숨겨진 의도 or 흥미로운 레퍼런스]
>
> 어디서 시작할까요? 아니면 처음부터 순서대로 볼까요?

사용자가 방향 선택 → 그 섹션부터 시작.

## Step 3: 섹션별 분석

각 섹션마다:

### 3-1. 원문 제시
해당 섹션 원문 인용.

### 3-2. 전체 맥락 설명
- 이 섹션이 글 전체에서 하는 역할
- 배경지식 필요 시 — 역사, 문화, 작가 의도, 레퍼런스 설명

### 3-3. 주목할 표현 (최대 3개)
단순 번역 금지. 각 표현마다:
- 표현 원문
- 한국어 의미
- **왜 이 맥락에서 이 표현인가** — 뉘앙스, 어감, 대안 표현과의 차이

### 3-4. 다음 행동 제시
> "다음 섹션으로 갈까요? 아니면 이 부분 더 파고들까요?"

사용자가 결정.

## 분석 깊이 원칙

- 언어 + 배경지식 항상 함께
- "이 단어 무슨 뜻?" 수준 금지
- "왜 이 단어를 여기서 썼는가"에 답할 것
- 노래 가사: 운율, 중의적 표현, 감정 흐름 중점
- 기사: 논리 구조, 필자 입장, 생략된 전제 중점
- 소설: 서사 장치, 캐릭터 심리, 시대·문화 배경 중점

## 응답 언어

- 설명·분석·배경: 한국어
- 원문 표현 인용: 원어 + 한국어 병기

## 저장

저장은 사용자가 직접 `/capture` 호출. Claude가 묻지 않음.

## Stop Rule

`그만`, `stop`, `여기까지`, `종료` → 즉시 종료.
