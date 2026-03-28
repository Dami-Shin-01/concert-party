# 콘서트파티 웹사이트 프로젝트 — 세션 로그

> 일시: 2026-03-27 ~ 2026-03-28
> 프로젝트: 공연기획 대행사 "콘서트파티" 웹사이트 신규 구축

---

## Phase 0: 에이전트 팀 인프라 구축

### 웹디자인 레퍼런스 수집 팀 구성
- `web-reference` 팀 생성
- **planner** 에이전트: 수집 계획 수립 → `plan.md` 작성
  - 6개 카테고리: 어워드 & 쇼케이스, 스크롤 애니메이션, 인터랙티브 모션, 3D 웹, 마이크로인터랙션, 타이포그래피
  - 수집 항목 양식 정의 (URL, 사이트 주제, 디자인 스타일, 모션 유형, 사용 기술, 주목할 특징)

### 레퍼런스 수집 (병렬 3명)
- **collector-1**: 디자인 어워드 & 쇼케이스 → 17개 수집 (`design-awards.md`)
- **collector-2**: 스크롤 애니메이션 & 인터랙티브 모션 → 15개 수집 (`motion-effects.md`)
- **collector-3**: 3D 웹 & 크리에이티브 코딩 → 20개 수집 (`3d-creative.md`)
- **summarizer**: 전체 종합 → 45개 고유 사이트 (`README.md`)

### 4인 역할 토론
- **pm** (기획자): UX 흐름, 정보 설계 관점 분석
- **marketer** (마케터): 브랜드 임팩트, CTA, 전환율 관점 분석
- **developer** (개발자): 기술 스택, 성능, 구현 난이도 관점 분석
- **designer** (웹디자이너): 비주얼, 타이포그래피, 모션 원칙 관점 분석
- **facilitator**: 종합 전략 수립 → `final-strategy.md`

### 종합 전략 합의 사항
- 디자인 방향: "절제된 대담함(Restrained Boldness)"
- 기술 스택: Next.js + Tailwind + GSAP ScrollTrigger + Lenis + Three.js(히어로 한정)
- TOP 5 벤치마크: Stripe, Linear, Cuberto, Dennis Snellenberg, Scout Motors

---

## Phase 1: 에이전트 팀 재구성 — 방법 2 (디렉터 + 커스텀 에이전트)

### 커스텀 에이전트 파일 생성 (`.claude/agents/`)
- `web-project-director.md` — 전체 파이프라인 자동 오케스트레이션
- `client-analyst.md` — 클라이언트 정보 분석
- `ref-collector.md` — 맞춤 레퍼런스 수집
- `web-pm.md` — 기획자
- `web-marketer.md` — 마케터
- `web-developer.md` — 개발자
- `web-designer.md` — 웹디자이너

### 디렉터 워크플로우
```
[클라이언트 정보 입력]
  → Phase 1: client-analyst → client-brief.md
  → Phase 2: ref-collector × 3 (병렬) → 맞춤 레퍼런스
  → Phase 3: 4인 토론 (pm + marketer + developer + designer)
  → Phase 4: 구축 계획서 (build-plan.md)
```

---

## Phase 2: 콘서트파티 프로젝트 착수

### 클라이언트 정보
- **회사명**: 콘서트파티
- **업종**: 공연기획 대행사
- **사업 내용**: 국내외 행사 기획 및 섭외 관리
- **타겟**: 공공기관 및 기업체 VIP 행사 기획
- **웹사이트 목적**: 포트폴리오 및 회사 소개
- **상태**: 신규 구축 (기존 웹사이트 없음)

### 1차 회의 확정 사항
- 웹사이트 신규 구축 확정
- 히어로 섹션에 트렌디한 3D 모션 적용 확정

### client-analyst 작업 결과
1. **client-brief.md** — 클라이언트 브리프 초안
   - 확정/[추정]/[미확인] 태그 구분
   - 경쟁사 14개 업체 조사 포함
2. **client-questions.md** — 클라이언트 질문서 (19개 질문, A~E 카테고리)
   - 확정 사항은 ✅ 1차 회의 확정 태그로 답변 완료 표시
   - 3D 모션 구체 방향 세부 질문 추가 (E-3-1, E-3-2)
3. **industry-references.md** — 유사 업종 레퍼런스 23개
   - Part A: 국내 공연기획/이벤트 대행사 11개
   - Part B: 해외 이벤트 에이전시 6개
   - Part C: 3D 모션 인상적인 사이트 6개
   - Part D: 히어로 3D 모션 4가지 방향 제안

---

## Phase 3: 5인 레퍼런스 검토 — 23개 → 12개 선별

### 검토 참여자
| 에이전트 | 역할 | 유지 수 |
|---------|------|--------|
| pm | 기획자 (UX/정보설계) | 14개 |
| marketer | 마케터 (브랜드/전환율) | 17개 |
| developer | 개발자 (기술/성능) | 12개 |
| designer | 웹디자이너 (비주얼/모션) | 14개 |
| client | 가상 클라이언트 (경영자 관점) | 15개 |

### 최종 선별 기준
- 4-5명 유지 → 자동 유지 (8개)
- 0-2명 유지 → 자동 제거 (9개)
- 3명 유지 → 개별 심의 (4개 중 3개 유지, 1개 제거)

### 최종 유지 12개

#### 만장일치 (5표, 8개)
1. **벤트리프로젝트** — 동종업계 유일한 모던 디자인 벤치마크
2. **Superfly** — 라이브 이벤트 에너지의 웹 전달
3. **Live Nation Entertainment** — 실적 수치 + 기업적 신뢰 톤
4. **CGHERO** — 3D 기술력의 웹 표현
5. **Lusion** — 인터랙티브 3D 히어로 최고 레퍼런스
6. **Active Theory** — 무대/조명 3D 재현
7. **Noomo Agency** — 3D 스토리텔링 스크롤 경험
8. **Epic** — 포트폴리오 시네마틱 전환 효과

#### 심의 후 유지 (3-4표, 4개)
9. **CJ ENM 엔터테인먼트** (4표) — UI 퀄리티 기준선, 영상 히어로 완성도
10. **현대기획사** (3표) — 공공기관 신뢰 배지/인증 배치 방식
11. **플레이컴** (3표) — 원스톱 프로세스 시각화 구조
12. **경성미디어그룹** (3표) — 공공기관 실적/고객사 로고 표현

#### 제거 (11개)
더플레이, 에픽엔터, 탑플랜, (주)행사기획, 이벤터스, 이벤트넷, CJ ENM Performing Arts, Bizzabo, Live Nation Productions, BDSN Club, Resn

### 히어로 3D 방향 합의
**무대 조명 + 파티클 결합** — 다크 톤 배경에 네온 조명 파티클이 마우스에 반응하는 형태. 5인 모두 "세련되면서도 가볍지 않다"고 합의.

---

## 현재 산출물 구조

```
/home/shin/web-projects/concert-party/
├── client-brief.md                    ← 클라이언트 브리프
├── client-questions.md                ← 클라이언트 질문서 (확정 사항 반영)
├── industry-references.md             ← 유사 업종 레퍼런스 (원본 23개)
├── industry-references-final.md       ← 5인 검토 후 최종 12개
├── session-log.md                     ← 본 파일
└── review/
    ├── pm-review.md                   ← 기획자 검토 결과
    ├── marketer-review.md             ← 마케터 검토 결과
    ├── developer-review.md            ← 개발자 검토 결과
    ├── designer-review.md             ← 웹디자이너 검토 결과
    └── client-review.md               ← 가상 클라이언트 검토 결과
```

### 기존 레퍼런스 DB (범용)
```
/home/shin/web-references/
├── plan.md                            ← 수집 계획서
├── design-awards.md                   ← 어워드 & 쇼케이스 (17개)
├── motion-effects.md                  ← 모션 & 인터랙션 (15개)
├── 3d-creative.md                     ← 3D & 크리에이티브 (20개)
├── README.md                          ← 전체 종합 (45개 고유 사이트)
└── discussion/
    ├── pm-perspective.md              ← 기획자 관점
    ├── marketer-perspective.md        ← 마케터 관점
    ├── developer-perspective.md       ← 개발자 관점
    ├── designer-perspective.md        ← 웹디자이너 관점
    └── final-strategy.md             ← 종합 토론 결과 & 적용 전략
```

---

## 다음 단계 (예정)

1. 클라이언트 질문서 회신 수령
2. 회신 기반 client-brief.md 업데이트
3. Phase 2: 맞춤 레퍼런스 수집 (ref-collector)
4. Phase 3: 4인 역할 토론 (콘서트파티 맥락)
5. Phase 4: 구축 계획서 작성 (build-plan.md)
