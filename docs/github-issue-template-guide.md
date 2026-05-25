# GitHub Issue Template Guide

이 문서는 `.github/ISSUE_TEMPLATE` 디렉터리에 구성된 Issue Template 파일들의 역할을 설명합니다.  
팀원들이 어떤 상황에서 어떤 템플릿을 사용해야 하는지 빠르게 이해하기 위한 안내 문서입니다.

---

## 전체 구조

```text
.github/
└── ISSUE_TEMPLATE/
    ├── feature.yml
    ├── bug.yml
    ├── docs.yml
    ├── decision.yml
    ├── troubleshooting.yml
    ├── sprint-backlog.yml
    ├── sprint-review.yml
    └── config.yml
```

---

## 템플릿별 설명

| 파일명                | 목적                                                             | 사용 시점                                                                            |
| --------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| `feature.yml`         | 새로운 기능 구현 또는 기존 기능 개선 작업을 정의합니다.          | 기능 개발을 시작하기 전에 작업 목적, 구현 항목, 완료 조건을 정리할 때 사용합니다.    |
| `bug.yml`             | 버그나 예상과 다른 동작을 기록합니다.                            | 오류가 발생했거나, 정상적으로 동작해야 하는 기능이 실패했을 때 사용합니다.           |
| `docs.yml`            | 문서 작성, 수정, 정리 작업을 관리합니다.                         | README, 기능 정의서, API 명세, 아키텍처 문서 등을 작성하거나 수정할 때 사용합니다.   |
| `decision.yml`        | 기술 선택이나 설계 방향에 대한 결정을 기록합니다.                | 특정 기술 스택, 아키텍처, 데이터 저장 방식, API 설계 방향 등을 결정할 때 사용합니다. |
| `troubleshooting.yml` | 문제 발생 원인과 해결 과정을 기록합니다.                         | 에러를 분석하고 해결한 과정을 재사용 가능한 기록으로 남기고 싶을 때 사용합니다.      |
| `sprint-backlog.yml`  | 이번 스프린트의 목표, 작업 범위, 산출물, 완료 기준을 정의합니다. | 스프린트 시작 시 이번 주기에서 무엇을 완료할지 계획할 때 사용합니다.                 |
| `sprint-review.yml`   | 스프린트 결과와 회고 내용을 기록합니다.                          | 스프린트 종료 후 완료한 작업, 미완료 작업, 배운 점, 개선점을 정리할 때 사용합니다.   |
| `config.yml`          | Issue Template 선택 화면의 동작을 설정합니다.                    | 빈 Issue 작성 허용 여부나 Discussion 안내 링크 등을 설정할 때 사용합니다.            |

---

## 사용 기준

### 1. 실제 구현 작업은 `feature.yml`

새로운 기능을 만들거나 기존 기능을 개선하는 작업은 `feature.yml`을 사용합니다.

예시:

```text
[Feature] 사용자 출발 위치 입력 기능 구현
[Feature] 중간 지점 계산 기능 구현
[Feature] 장소 추천 API 구현
```

---

### 2. 오류 수정은 `bug.yml`

재현 가능한 오류, 예상과 다른 동작, 실패하는 요청은 `bug.yml`을 사용합니다.

예시:

```text
[Bug] 위치 입력 API 요청 시 500 에러 발생
[Bug] 잘못된 주소 입력 시 예외 처리가 되지 않음
```

---

### 3. 문서 작업은 `docs.yml`

공통 기획 문서, 기능 정의서, API 명세, README 수정 등은 `docs.yml`을 사용합니다.

예시:

```text
[Docs] 공통 기능 정의서 작성
[Docs] 추천 API 명세 작성
[Docs] 프로젝트 README 수정
```

---

### 4. 기술 선택과 설계 결정은 `decision.yml`

각자 다른 방식으로 구현하는 프로젝트이므로, 기술 선택의 이유를 기록하는 것이 중요합니다.  
단순히 “무엇을 선택했는지”가 아니라 “왜 선택했는지”를 함께 남깁니다.

예시:

```text
[Decision] Vector DB 선택 기준 정리
[Decision] RAG 파이프라인 구조 결정
[Decision] 장소 데이터 저장 방식 결정
```

---

### 5. 문제 해결 기록은 `troubleshooting.yml`

해결한 문제를 단순히 지나치지 않고, 원인과 해결 과정을 남길 때 사용합니다.  
나중에 회고, 발표, 포트폴리오 자료로 활용할 수 있습니다.

예시:

```text
[Troubleshooting] 2026-05-25 - API 토큰 인증 오류
[Troubleshooting] 2026-05-26 - CORS 설정 오류
```

---

### 6. 스프린트 시작 시 `sprint-backlog.yml`

스프린트 시작 전에 이번 스프린트의 목표, 포함할 작업, 산출물, 완료 기준을 정의합니다.  
실제 세부 작업은 별도의 Feature, Docs, Decision Issue로 분리해서 관리하는 것을 권장합니다.

예시:

```text
[Sprint Backlog] Sprint 1 - 공통 기능 정의
[Sprint Backlog] Sprint 2 - MVP 기능 구현
```

---

### 7. 스프린트 종료 시 `sprint-review.yml`

스프린트가 끝난 뒤 결과와 회고를 정리합니다.  
완료한 작업, 완료하지 못한 작업, 배운 점, 다음 스프린트 개선점을 기록합니다.

예시:

```text
[Sprint Review] Sprint 1 - 공통 기능 정의
[Sprint Review] Sprint 2 - MVP 기능 구현
```

---

### 8. 템플릿 설정은 `config.yml`

`config.yml`은 개별 Issue 템플릿이 아니라, Issue Template 전체의 설정 파일입니다.

주로 다음을 설정합니다.

```text
- 빈 Issue 작성 허용 여부
- Discussion, 문서, 외부 링크 안내
```

예를 들어, 아직 작업으로 확정되지 않은 아이디어나 질문은 Issue가 아니라 Discussion으로 유도할 수 있습니다.

---

## 권장 운영 방식

| 상황                       | 권장 템플릿           |
| -------------------------- | --------------------- |
| 기능을 구현한다            | `feature.yml`         |
| 버그를 수정한다            | `bug.yml`             |
| 문서를 작성하거나 수정한다 | `docs.yml`            |
| 기술 선택을 기록한다       | `decision.yml`        |
| 문제 해결 과정을 남긴다    | `troubleshooting.yml` |
| 스프린트를 계획한다        | `sprint-backlog.yml`  |
| 스프린트를 회고한다        | `sprint-review.yml`   |

---

## 기본 원칙

1. **Issue는 작업 단위로 작성합니다.**
   - 하나의 Issue에는 하나의 목적만 담는 것을 권장합니다.

2. **완료 조건을 명확히 작성합니다.**
   - 완료 기준이 모호하면 작업 완료 여부를 판단하기 어렵습니다.

3. **논의와 작업을 구분합니다.**
   - 아직 결정되지 않은 아이디어나 질문은 Discussion에서 먼저 논의합니다.
   - 작업으로 확정된 내용은 Issue로 등록합니다.

4. **기술 선택의 이유를 기록합니다.**
   - 이 프로젝트는 같은 주제를 각자 다른 방식으로 구현하므로, 선택의 근거가 중요합니다.

5. **트러블슈팅은 재사용 가능한 지식으로 남깁니다.**
   - 단순 에러 기록이 아니라 원인, 해결 방법, 재발 방지 방법까지 정리합니다.

---

## 추천 흐름

```text
Discussion에서 아이디어 논의
        ↓
decision.yml로 기술 결정 기록
        ↓
sprint-backlog.yml로 스프린트 계획
        ↓
feature.yml / docs.yml / bug.yml로 세부 작업 관리
        ↓
PR 생성 및 리뷰
        ↓
troubleshooting.yml로 문제 해결 과정 기록
        ↓
sprint-review.yml로 스프린트 회고
```
