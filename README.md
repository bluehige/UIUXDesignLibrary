# UI/UX Design Library

UI/UX가 필요할 때 **실제 제품 패턴, 공식 디자인 시스템, UX 제작 원칙, 접근성, 게임 UI, 안전교육·키오스크·VR, AI 작업 스킬**을 한 곳에서 참고하기 위한 라이브러리입니다.

- 기준일: 2026-08-12
- 적용 범위: Web / Mobile / Desktop / Dashboard / Kiosk / VR·360 / Game / Safety Training
- 자료 원칙: `공식 표준·연구 → 실제 출시 제품 → 전문 큐레이션 → 시각 영감` 순으로 신뢰도를 구분합니다.

## 바로 열기

- **Live Library (GitHub Pages)**: https://bluehige.github.io/UIUXDesignLibrary/
- **즉시 HTML 미리보기**: https://raw.githack.com/bluehige/UIUXDesignLibrary/main/index.html
- **통합 프로젝트 지식소스**: [`UI_UX_PROJECT_SOURCE.md`](UI_UX_PROJECT_SOURCE.md)

`index.html`은 별도 빌드가 필요 없는 단일 정적 HTML이며, 자료를 카테고리와 검색어로 필터링할 수 있습니다.

## 가장 빠른 사용법

1. `templates/PROJECT_BRIEF.md`로 사용자·과업·플랫폼·제약을 정리합니다.
2. `01_REFERENCE_SITES.md`에서 실제 제품 사례 3개, 공식 기준 1개, 반례 1개를 고릅니다.
3. `02_DESIGN_SYSTEMS.md`에서 플랫폼·도메인에 맞는 기준 시스템 1~2개를 고릅니다.
4. `skills/ui-ux-design-director/SKILL.md`로 정보 구조, 흐름, 화면, 상태, 디자인 시스템을 설계합니다.
5. `skills/ui-ux-auditor/SKILL.md`로 독립 검수합니다.
6. 게임은 `game-ui-overlay`, 안전교육·아동·키오스크·VR은 `safety-training-ui-overlay`를 추가합니다.

## 문서

- `01_REFERENCE_SITES.md` — UI/UX 레퍼런스 사이트 카탈로그
- `02_DESIGN_SYSTEMS.md` — Material, Apple HIG, Fluent, Carbon, KRDS, SEED 등
- `03_UX_UI_PRINCIPLES.md` — Nielsen 휴리스틱, UX 법칙, 정보 구조·오류·피드백 원칙
- `04_ACCESSIBILITY.md` — WCAG 2.2, KWCAG 2.2, 키보드·포커스·터치·모션 검수
- `05_GAME_AND_SPECIAL_UI.md` — 게임, 비주얼 노블, 키오스크, VR·360, 안전교육
- `06_AI_SKILLS_CATALOG.md` — UI/UX 관련 AI 스킬과 역할 조합
- `07_WORKFLOW_AND_SCORECARD.md` — 제작 프로세스와 100점 검수표
- `08_GLOSSARY.md` — UI/UX 실무 용어집

## 운영 원칙

- 레퍼런스 화면과 에셋을 1:1 복제하지 않습니다.
- 시각 스타일보다 사용자 과업과 실패 비용을 먼저 정의합니다.
- 생성용 스킬과 검수용 스킬을 분리합니다.
- 접근성은 마지막 검사가 아니라 브리프·구조·컴포넌트 단계부터 적용합니다.
- 실제 콘텐츠, 긴 문장, 로딩·빈 상태·오류·성공 상태를 넣어 검증합니다.
- 외부 사이트·스킬의 가격, URL, 공개 범위, 버전은 변경될 수 있으므로 사용 시점에 다시 확인합니다.

## GitHub Pages

이 저장소에는 `.github/workflows/pages.yml`을 포함해 정적 `index.html`을 GitHub Pages에 배포하도록 구성합니다. 저장소에서 Pages가 아직 한 번도 활성화되지 않았다면 GitHub의 `Settings → Pages → Source → GitHub Actions`를 한 번 선택해야 할 수 있습니다.
