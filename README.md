# mypage

JM의 개인 포트폴리오 홈페이지입니다. **순수 HTML/CSS/JS 단일 파일(`index.html`)**로 구성되어, 빌드 도구 없이 브라우저에서 바로 열어 확인할 수 있습니다.

## 미리보기

- 배포 링크(GitHub Pages): `https://jungmin1811.github.io/mypage/`
- 배포 링크(Vercel): `https://mypage-one-bay.vercel.app/`
- 데모(최근 프로젝트 링크): `https://jungmin1811.github.io/todo-app-0506/`

## 실행 방법

### 브라우저에서 바로 열기

```powershell
start index.html
```

### (선택) Live Server로 실행

- VS Code의 Live Server 확장으로 `index.html`을 열어 로컬 서버에서 확인할 수 있습니다.

## 주요 기능

- **라이트/다크 테마**: CSS 변수(`:root`, `[data-theme="dark"]`) 기반, 사용자 선택을 `localStorage`에 저장
- **섹션 내비게이션**: 상단 메뉴에서 섹션으로 부드러운 스크롤 이동(`scrollToSection`)
- **스크롤 리빌 애니메이션**: `IntersectionObserver`로 `.reveal` 요소에 `.visible` 적용
- **포트폴리오 모달**: 카드 클릭 시 모달 팝업, `projects[]` 데이터로 동적 렌더링(`openModal`)
- **블로그 섹션**: 현재 Coming Soon 상태(추후 콘텐츠 추가용)

## 커스터마이징 가이드

### 프로젝트(Portfolio) 추가/수정

1. `index.html`의 `projects[]` 배열에 프로젝트 객체를 추가/수정합니다.
2. `#portfolio` 섹션의 `.proj-grid`에 카드 HTML을 추가/수정하고, `onclick="openModal(n)"` 인덱스를 맞춥니다.

### 연락처(Contact) 수정

- `#contact` 섹션의 GitHub 링크/이메일(`mailto:`)을 본인 정보로 바꾸면 됩니다.

### 테마 컬러 변경

- `index.html`의 `:root`, `[data-theme="dark"]`에 정의된 CSS 변수 값을 조정하면 전체 톤이 바뀝니다.

## 폴더 구조

```text
mypage/
  index.html
  docs/
    개인홈페이지_기능분석.md
  CLAUDE.md
```

## 참고

- 빌드/테스트/린트 과정이 없어서, 수정 후 브라우저 새로고침으로 확인합니다.

