# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

JM의 개인 포트폴리오 홈페이지. 순수 HTML/CSS/JS로 작성된 단일 파일(`index.html`) 프로젝트로, 빌드 도구나 패키지 매니저 없이 브라우저에서 직접 열어 확인한다.

## 개발 방법

```powershell
# 브라우저에서 직접 열기
start index.html

# 또는 VS Code Live Server 확장으로 로컬 서버 실행
```

빌드·테스트·린트 단계 없음. 수정 후 브라우저 새로고침으로 확인.

## 아키텍처

`index.html` 단일 파일에 HTML/CSS/JS가 모두 포함된 구조:

- **CSS 변수 테마 시스템** — `:root`와 `[data-theme="dark"]`에 CSS 변수(`--bg`, `--text`, `--accent` 등)를 선언해 라이트/다크 전환을 처리
- **포트폴리오 모달** — `projects[]` 배열에 데이터를 선언하고 `openModal(idx)`가 동적으로 모달 HTML을 생성
- **스크롤 애니메이션** — `IntersectionObserver`로 `.reveal` 클래스 요소를 감지해 `.visible` 클래스를 추가
- **섹션 내비게이션** — `scrollToSection(id)`로 smooth scroll 처리

## 주요 기능 확장 포인트

- **프로젝트 추가**: `index.html` 내 `projects[]` 배열에 객체 추가 후 `.proj-grid`에 카드 HTML 추가
- **블로그 섹션**: 현재 "Coming Soon" 상태 — `#blog` 섹션에 실제 콘텐츠 추가 예정
- **연락처 폼**: 현재 mailto 링크만 있음 — EmailJS 또는 Formspree 연동으로 폼 방식 전환 고려
- **다크모드 지속성**: 현재 새로고침 시 초기화됨 — `localStorage`로 테마 상태 저장 가능

## 주석 규칙

코드에 주석을 달 때는 **항상 한글**로 작성한다.
