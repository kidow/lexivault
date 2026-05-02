---
name: spark
description: Picks a random language topic and delivers it in a "그거 아시나요?" style — real-life context, cultural backstory, mnemonic hook, then 1-2 situational practice questions. Use when the user runs /spark or /spark 일본어 or any language variant.
---

# Spark

## Purpose

Pick one language topic at random and teach it in an engaging, memorable way — not a textbook drill, but a story-first discovery.

One topic per session. User calls `/spark` again for the next one.

## Trigger

`/spark` — language optional.

Examples:
```
/spark
/spark 일본어
/spark 프랑스어
/spark 독일어
```

## Language Selection

- If language specified → use it.
- If omitted → pick any language from: 일본어, 프랑스어, 독일어, 중국어, 스페인어.

## Topic Selection

Pick freely. Mix vocabulary themes and situational contexts.

Good topic types:
- 일상 상황 표현 (카페, 대중교통, 쇼핑, 날씨 대화)
- 감정/뉘앙스 어휘 (한국어에 딱 맞는 번역이 없는 단어)
- 문화적으로 흥미로운 표현 (욕, 속담, 관용구)
- 발음 함정 / 혼동하기 쉬운 표현 쌍

Avoid: pure grammar rules without context, overly formal/academic topics.

## Response Format

### 1. 그거 아시나요? 훅

첫 줄은 반드시 흥미로운 질문이나 상황으로 시작. "그거 아시나요?" 또는 비슷한 방식으로.

### 2. 핵심 표현

목표 언어 표현 + 한국어 의미 + 발음 가이드 (필요 시).

### 3. 비하인드 / 문화 포인트

왜 이 표현이 존재하는지, 어떤 맥락에서 쓰이는지, 재미있는 어원·역사·문화적 배경. 단순 예문 나열 금지.

### 4. 기억 훅 (선택)

연상법, 어원 연결, 한국어와의 유사점 등 — 외우기 쉽게.

### 5. 실전 연습 (1-2문제)

상황을 제시하고 해당 표현을 쓰게 함. 정답 하나만 있는 빈칸 금지.

예시:
> "친구가 약속 장소에 30분 늦게 도착했어요. 친구한테 뭐라고 할까요? 오늘 배운 표현을 써보세요."

사용자가 답하면 → 간결한 피드백 + 자연스러운 변형 표현 1개 제시.

## After Practice

연습 끝나면 이렇게 마무리:
> "저장하고 싶으면 `/capture`로 남겨두세요. 다음 주제는 `/spark`!"

저장 여부는 묻지 않음. 사용자가 직접 결정.

## Response Language

- 설명·문화 배경·피드백: 한국어
- 핵심 표현·예문: 목표 언어 + 한국어 병기

## Stop Rule

사용자가 `그만`, `stop`, `여기까지` → 즉시 종료. 마무리 멘트 한 줄 이하.
