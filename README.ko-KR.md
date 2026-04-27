<p align="center">
  <a href="README.md">English</a> | 
  <a href="README.ko-KR.md">한국어</a>
</p>

# Lexivault

Lexivault는 Obsidian vault를 기반으로 외국어 학습 지식을 저장하고 복습하기 위한 개인 지식 베이스입니다.

기본 흐름은 Obsidian에 학습 내용을 구조화해 저장하고, 반복해서 떠올려야 하는 항목은 Anki 복습 대상으로 표시하는 방식입니다. 부가적으로 Codex의 `drill` 스킬을 사용하면 vault에 저장된 내용을 바탕으로 대화형 퀴즈를 진행할 수 있습니다.

## 목적

- Obsidian: 외국어 지식, 예문, 문법, 발음, 표현, 출처를 장기 보관합니다.
- Anki: 능동 회상이 필요한 내용을 반복 복습합니다.
- AnkiWeb: Anki 데스크톱과 모바일 환경을 동기화합니다.
- Codex skills: 학습 자료 저장과 대화형 퀴즈를 보조합니다.

## 구조

- `00_Inbox/`: 아직 정리하지 않은 임시 학습 자료를 둡니다.
- `01_Languages/`: 언어별 원본 노트를 저장합니다.
- `02_Review/`: 복습 대기 항목, Anki 후보, 복습 로그를 둡니다.
- `03_Templates/`: 노트 작성 템플릿을 둡니다.
- `04_Resources/`: 사전, 책, 외부 자료, 참고 문서를 둡니다.
- `05_Dashboard/`: 학습 현황과 복습 진입점을 둡니다.
- `.codex/skills/`: 이 vault에서 사용하는 Codex 스킬을 둡니다.

`01_Languages/` 아래에는 언어별 폴더가 있고, 각 언어는 보통 `Vocabulary`, `Grammar`, `Sentences`, `Expressions`, `Pronunciation`, `Sources` 같은 분류로 나뉩니다.

## 주요 워크플로

### 1. Capture

`capture` 스킬은 새로 배운 외국어 자료를 올바른 언어와 분류 폴더에 저장합니다.

주요 동작은 다음과 같습니다.

- 입력 내용을 어휘, 문법, 문장, 표현, 발음, 출처 중 하나로 분류합니다.
- 언어를 판단하고, 중국어는 방언과 문자 변형도 구분합니다.
- 중복 가능성이 있으면 기존 노트를 먼저 확인합니다.
- YAML frontmatter와 본문 구조를 맞춰 노트를 생성하거나 갱신합니다.
- 능동 회상 가치가 있는 자료만 `anki: true`로 표시합니다.

언어, 노트 유형, 중국어 변형, 중복 병합 여부가 불명확하면 바로 쓰지 않고 먼저 질문하는 규칙을 따릅니다.

### 2. Anki Review

Anki는 Obsidian 노트 전체를 그대로 외우는 도구가 아니라, 반복 회상이 필요한 최소 단위만 복습하는 도구로 사용합니다.

권장 흐름은 다음과 같습니다.

1. Obsidian에 학습 내용을 먼저 정리합니다.
2. 복습 가치가 있는 항목에만 `anki: true`를 표시합니다.
3. `02_Review/Anki_Candidates/` 또는 관련 리뷰 문서를 통해 카드화 후보를 관리합니다.
4. Anki에서는 간단하고 명확한 질문-답변 형태로 복습합니다.

### 3. Drill

`drill` 스킬은 vault 안의 학습 내용을 바탕으로 대화형 퀴즈를 진행합니다.

- 한 번에 한 문제씩 냅니다.
- 사용자의 답변을 기다립니다.
- 짧게 교정하고 다음 문제로 넘어갑니다.
- 기본적으로 Anki 카드를 만들지 않고, drill 기록도 vault에 저장하지 않습니다.

예시:

```text
/drill 일본어 전체
/drill 오늘 배운 것
/drill 일주일 이내 배웠던 것들
```

## 매일 사용하는 법

1. 새로 배운 내용은 먼저 빠르게 기록합니다.
2. 정리할 때 `capture` 스킬로 언어와 유형에 맞는 노트로 옮깁니다.
3. 복습할 때는 `05_Dashboard/Study Dashboard.md`에서 시작합니다.
4. 암기해야 할 항목은 Anki 후보로 관리합니다.
5. 대화형으로 점검하고 싶을 때는 `drill` 스킬을 사용합니다.

## 참고 문서

- [Obsidian Anki Guide.md](Obsidian%20Anki%20Guide.md): Obsidian과 Anki를 함께 쓰는 운영 규칙
- [.codex/skills/capture/SKILL.md](.codex/skills/capture/SKILL.md): 학습 자료 저장 스킬
- [.codex/skills/drill/SKILL.md](.codex/skills/drill/SKILL.md): 대화형 퀴즈 스킬
