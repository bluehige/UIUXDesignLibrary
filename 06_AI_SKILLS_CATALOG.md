# AI UI/UX 스킬 카탈로그와 조합 원칙

## 외부 스킬

| 스킬 | 역할 | 강점 | 주의점 |
|---|---|---|---|
| [Anthropic Frontend Design](https://github.com/anthropics/skills/tree/main/skills/frontend-design) | 의도적이고 차별화된 프런트엔드 생성 | 전형적인 AI 템플릿 외형을 피하도록 유도 | 전체 UX 연구와 접근성 감사를 대신하지 않음 |
| [Vercel Web Design Guidelines](https://github.com/vercel-labs/agent-skills/tree/main/skills/web-design-guidelines) | 웹 UI 코드 검수 | 생성보다 리뷰 역할이 명확 | 웹·React 편향 가능, 외부 최신 규칙은 버전 고정 필요 |
| [UI UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | 스타일·팔레트·폰트·제품 유형·기술 스택 탐색 | 범위가 넓고 여러 스택 지원 | 넓은 만큼 결과가 피상적일 수 있어 프로젝트 전용 브리프 필수 |
| [Senior Designer Skill](https://github.com/sshahzaiib/senior-designer-skill) | 근거 기반 판단과 점수형 검수 | 출처와 검증 절차 강조 | 커뮤니티 프로젝트이므로 규칙 출처·충돌 직접 검토 |
| [jakubkrehel/skills](https://github.com/jakubkrehel/skills) | UI 폴리시·모션·접근성·문구 등 세부 작업 | 작업별 작은 스킬로 분리 | 핵심 디자인 원칙을 먼저 고정해야 함 |
| [Accessibility Agents](https://github.com/Community-Access/accessibility-agents) | WCAG 중심 전문 접근성 검수 | 여러 전문 역할로 검수를 분리 | 실제 키보드·스크린리더 테스트를 대체하지 않음 |
| [Awesome UX Skills](https://github.com/tommyjepsen/awesome-ux-skills) | UX 스킬 탐색 디렉터리 | 새로운 스킬 발견에 유용 | 목록 등재가 품질 보증은 아님 |

## 이 라이브러리에 포함된 핵심 스킬

| 스킬 | 역할 |
|---|---|
| `ui-ux-design-director` | 브리프 정규화, 레퍼런스 분석, 흐름, 토큰, 화면·상태 명세 |
| `ui-ux-auditor` | 휴리스틱, 접근성, 일관성, 입력, 구현 가능성의 독립 검수 |
| `game-ui-overlay` | HUD, 컨트롤러, 게임 상태, 튜토리얼, 실제 플레이 가독성 보강 |
| `safety-training-ui-overlay` | 안전교육, 어린이, 키오스크, VR, 현지화, 법령 위험 보강 |

## 권장 조합

### 신규 UI 제작

```text
주도: ui-ux-design-director
시각 확장: Anthropic Frontend Design 또는 UI UX Pro Max 중 1개
독립 검수: ui-ux-auditor
웹 코드 검수: Vercel Web Design Guidelines
```

### 기존 UI 개선

```text
주도: ui-ux-auditor
근거: Nielsen 10 + 플랫폼 HIG + WCAG/KWCAG
시각 개선: Anthropic Frontend Design
재검수: ui-ux-auditor
```

### 게임 UI

```text
주도: ui-ux-design-director
오버레이: game-ui-overlay
레퍼런스: Game UI Database + 실제 플레이 영상
검수: ui-ux-auditor
```

### 안전교육·키오스크·VR

```text
주도: ui-ux-design-director
오버레이: safety-training-ui-overlay
기준: KRDS + KWCAG/WCAG + 해당 국가 법령·기관 지침
검수: ui-ux-auditor + 실제 환경 테스트
```

## 스킬 운용 규칙

1. **한 개의 주도 스킬**이 브리프와 우선순위를 결정합니다.
2. 다른 스킬은 `시각 확장`, `접근성`, `코드 리뷰`처럼 역할을 좁힙니다.
3. 외부 스킬이 프로젝트 브리프·공식 표준과 충돌하면 사용자 과업과 공식 기준을 우선합니다.
4. 저장소의 최신 main을 매번 자동으로 불러오면 결과 재현성이 떨어질 수 있으므로 커밋 또는 릴리스 버전을 고정합니다.
5. 설치 전 라이선스, 실행 스크립트, 네트워크 요청, 파일 읽기·쓰기 범위, 종속성, 유지보수, 규칙의 출처를 확인합니다.
6. 스킬이 제시한 색상·폰트·스타일을 정답으로 취급하지 않습니다.
7. 생성 결과는 반드시 별도의 감사 스킬이나 사람의 검토를 통과시킵니다.

## 외부 스킬 도입 평가표

| 항목 | 질문 | 판정 |
|---|---|---|
| 목적 | 생성·검수·접근성·코드 중 역할이 명확한가? | 필수 |
| 근거 | 규칙의 출처와 버전이 적혀 있는가? | 필수 |
| 재현성 | 같은 버전으로 다시 실행할 수 있는가? | 권장 |
| 보안 | 외부 명령·네트워크·파일 쓰기 범위가 안전한가? | 필수 |
| 범위 | 프로젝트 브리프와 충돌하지 않는가? | 필수 |
| 유지보수 | 최근 변경과 이슈 대응이 확인되는가? | 권장 |
| 라이선스 | 사용·수정·배포 조건이 명확한가? | 필수 |
