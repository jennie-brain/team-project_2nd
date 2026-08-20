# PRD 작성 방법론 — CardFit (메타프롬프팅 적용)

> 사용자가 제시한 원본 프롬프트(시니어 제품 아키텍트 페르소나, Pain/JTBD/Desired Outcome/Differential Value/Proof 5원칙 + 9절 템플릿)를 CardFit 프로젝트에 맞게 메타프롬프팅으로 최적화한 버전입니다. `{Value Proposition Sheet}`·`{PRD 초안 디렉토리}` 두 플레이스홀더를 채우고, 우리 프로젝트에서 이미 확정된 산출물(AOS·DOS·JTBD·Value Chain·KSF·경쟁사 분석)을 규칙마다 명시적으로 연결해 "일반적인 PRD 프롬프트"가 아니라 "CardFit 전용 실행 프롬프트"로 만들었습니다.

---

## 0. 메타프롬프팅 — 무엇을, 왜 바꿨는가

| 원본 규칙 | 문제(일반 프롬프트로 실행 시) | 최적화 |
| --- | --- | --- |
| 입력 = `{Value Proposition Sheet}` | 플레이스홀더만 있으면 어떤 VPS를 쓸지, 최신본인지 알 수 없음 | `효진/확정본/08_Value_Proposition.md`로 고정 — 이미 Fit 검사(3절)까지 끝난 확정본이라 별도 재해석 없이 그대로 인용 |
| 1. Pain/Needs 수치화 | "예: 가입 전환율 30% 미달" 같은 예시가 일반적이라, 우리 프로젝트 고유 지표(Payment Plan Selection Rate, 민원 +88.4% 등)를 놓치기 쉬움 | VP Sheet 1-2절 Pain 7개 + `윤정/확정본/03_KSF.md`·Evidence Log의 기존 수치를 실패 KPI로 직접 매핑 |
| 2. JTBD → GWT + AC | 어떤 Job을 스토리로 만들지 기준이 없으면 6개 후보를 전부 동등하게 다뤄 우선순위가 흐려짐 | `가람/확정본/07_JTBD.md` 0절 Job 선언 + AOS·DOS 우선순위(A·C 공동 1위, F 니치)를 그대로 스토리 우선순위로 사용 — **A·C·B·F 순으로만 GWT 작성**, D·E는 Should/Won't로 축약 |
| 3. Desired Outcome → KPI | "북극성 KPI"를 새로 만들면 기존에 확정된 지표(Payment Plan Selection Rate, 피치덱 8장)와 충돌할 위험 | 북극성 KPI는 기존 지표를 그대로 승계하고, VP Sheet 5절 미해결 항목 #2(KPI 사각지대)에서 지적된 **실행 완주율(Execution Completion Rate)**을 보조 KPI로 신설 |
| 4. Differential Value 수치 비교 | "성능/정확도/비용" 프레임은 SaaS 일반형이라 카드추천 시장에 안 맞음 | `가람/0820/경쟁사 분석 결과.md`의 5개 경쟁사 비교로 대체 — "미래소비반영 여부", "조합 재배치 여부", "근거공개 수준" 3축으로 차별화 수치화 |
| 5. Proof = 실험 설계 | 일반 A/B 테스트 예시만 있으면 우리가 이미 계획한 Concierge Test(피치덱 9장)를 놓침 | Concierge Test를 1차 실험으로 명시하고, 이후 A/B 테스트는 그 다음 단계로 배치 |
| 출력 규칙: **F-05(실행 지원) 관련 서술 금지** | 원본 프롬프트에는 없는 규칙이지만, 최근 팀 결정(마이데이터 기반 서비스는 해지·전환 실행에 대한 직권·대행 권한이 없음, `윤정/확정본/02_Value_Chain.md` 5절)을 PRD가 위반하면 안 됨 | **메타프롬프팅으로 신규 추가**: PRD의 어떤 절에서도 "해지 대행", "실행 안내", "만류 대응 안내" 등 실행 지원 기능을 제안하지 않는다. 후보 C(실행완주)의 공백은 **측정(실행 완주율 KPI)으로만 대응**하고 기능으로 메우지 않는다 |

---

## 1. 최종 프롬프트 (실행용)

```markdown
# Persona
당신은 CardFit(미래지출 결제설계 서비스)의 시니어 제품 아키텍트입니다.

# Aim
`효진/확정본/08_Value_Proposition.md`(Value Proposition Sheet)를 기반으로 PRD(제품 요구사항 문서)를 작성하세요.
PRD는 아래 규칙과 구조를 반드시 따르세요.

# Rules
1. Pain/Needs — VP Sheet 1-2절 Pain 7개 각각을 실패 KPI와 함께 수치화한다. 기존에 확정된 수치(민원 +88.4%, 경쟁사 미래소비반영 0/6곳 등)를 우선 사용하고, 없으면 팀 추정치임을 🟡로 표기한다.
2. JTBD — `가람/확정본/07_JTBD.md` 0절 Job 선언 중 AOS·DOS 우선순위가 높은 A·C·B·F를 Given-When-Then 사용자 스토리로 변환한다. 각 스토리에 최소 3개의 Acceptance Criteria(측정 가능한 임계치 포함)를 작성한다. D·E는 Should/Won't로만 간단히 언급한다.
3. Desired Outcome — 북극성 KPI는 기존 Payment Plan Selection Rate를 승계하고, 보조 KPI로 Execution Completion Rate(측정 전용, 대행 아님)를 신설한다. 각 KPI에 기준선·목표값·측정 주기를 명시한다.
4. Differential Value — `가람/0820/경쟁사 분석 결과.md`의 5개 경쟁사 대비 "미래소비반영·조합재배치·근거공개" 3축 중 2가지 이상을 수치/등급으로 비교한다.
5. Proof — Concierge Test(피치덱 9장)를 1차 실험으로 연결하고, 이후 단계의 A/B 테스트 설계를 이어붙인다.
6. **금지 규칙**: 어떤 절에서도 해지·전환 실행 대행/상담/안내 기능을 제안하지 않는다. 후보 C(실행완주)의 공백은 Execution Completion Rate 측정으로만 대응한다(`윤정/확정본/02_Value_Chain.md` 5절 근거).

# Output
결과물은 PRD Markdown 형식으로만 작성한다. 구조적 가시성을 위해 계층 구조를 지키고, 복잡한 로직·사용자 여정은 Mermaid 다이어그램으로 삽입한다.
출력 경로: `가람/0820/PRD 초안.md`
```

---

## 2. 실행 결과

이 프롬프트를 실행한 결과물은 `가람/0820/PRD 초안.md`에 있습니다.

---

**연결 문서**: `효진/확정본/08_Value_Proposition.md`(VPS, 입력) · `가람/확정본/05~07`(CJM·AOS-DOS·JTBD) · `윤정/확정본/01~04`(Five Forces·Value Chain·KSF·TAM-SAM-SOM) · `가람/0820/경쟁사 분석 결과.md` · `가람/0820/PRD 초안.md`(출력)
