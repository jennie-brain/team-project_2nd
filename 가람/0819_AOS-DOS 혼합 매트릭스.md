# AOS–DOS 혼합 매트릭스 — 미래지출 결제설계 서비스

> `가람/0819_AOS 분석 결과.md`의 AOS 점수(X축)와 `가람/0819_DOS 분석 결과.md`의 DOS 점수(Y축)를 같은 항목끼리 대조한 혼합 매트릭스입니다. 두 분석 모두 점수가 존재하는 항목은 이서연의 Pain 3건(=AOS 후보 A·B·C)뿐이라, 이 3건만 배치했습니다. D·E·F는 DOS를 아직 채점하지 않아 이 매트릭스에는 없습니다(`가람/0819_DOS 분석 방법론.md` 다음 액션 참고).
>
> 사분면 경계선은 참고 이미지와 동일하게 **실제 값의 평균**(고정된 0.5가 아니라 이 3개 점의 AOS·DOS 평균)을 기준으로 그었습니다. ⚠️ 점이 3개뿐이라 평균 자체가 점들 중 하나와 거의 겹치는 경계 사례가 생깁니다 — 참고 이미지(점 30개)만큼 안정적인 분할은 아니라는 점을 감안해 주세요.

---

## 원본 점수

| 후보 | Pain | AOS | DOS(SOM 버전) | DOS(SAM 버전) |
| --- | --- | --- | --- | --- |
| A | 미래지출-카드혜택 자동 연결 | 4.0 | 4.0 | 2.8 |
| C | 실행(해지·전환) 완주 | 3.2 | 2.7 | 1.8 |
| B | 신뢰 가능한 계산 근거 | 2.4 | 1.8 | 1.2 |

---

## 혼합 매트릭스 — SOM 버전 (평균 AOS 3.20, DOS 2.83)

<svg width="760" height="600" xmlns="http://www.w3.org/2000/svg">
  <rect x="0" y="0" width="760" height="600" fill="#1b1b1b"/>
  <text x="380" y="35" text-anchor="middle" fill="#f0f0f0" font-size="19" font-family="sans-serif" font-weight="bold">AOS x DOS - SOM - AOS 3.20, DOS 2.83</text>

  <rect x="80" y="60" width="570" height="460" fill="none" stroke="#888888" stroke-width="1.5"/>
  <line x1="365" y1="60" x2="365" y2="520" stroke="#888888" stroke-width="1.5"/>
  <line x1="80" y1="311" x2="650" y2="311" stroke="#888888" stroke-width="1.5"/>

  <text x="222" y="82" text-anchor="middle" fill="#dddddd" font-size="15" font-family="sans-serif">시장 주도</text>
  <text x="507" y="82" text-anchor="middle" fill="#dddddd" font-size="15" font-family="sans-serif">최우선</text>
  <text x="222" y="332" text-anchor="middle" fill="#dddddd" font-size="15" font-family="sans-serif">후순위</text>
  <text x="507" y="332" text-anchor="middle" fill="#dddddd" font-size="15" font-family="sans-serif">니치</text>

  <circle cx="584" cy="131" r="6" fill="#cccccc"/>
  <text x="584" y="118" text-anchor="middle" fill="#f5f5f5" font-size="13" font-family="sans-serif">A 미래지출연결</text>
  <text x="584" y="150" text-anchor="middle" fill="#bbbbbb" font-size="12" font-family="sans-serif">AOS 4.0, DOS 4.0</text>

  <circle cx="365" cy="331" r="6" fill="#cccccc"/>
  <text x="365" y="365" text-anchor="middle" fill="#f5f5f5" font-size="13" font-family="sans-serif">C 실행완주</text>
  <text x="365" y="381" text-anchor="middle" fill="#bbbbbb" font-size="12" font-family="sans-serif">AOS 3.2, DOS 2.7</text>

  <circle cx="146" cy="469" r="6" fill="#cccccc"/>
  <text x="146" y="456" text-anchor="middle" fill="#f5f5f5" font-size="13" font-family="sans-serif">B 신뢰근거</text>
  <text x="146" y="488" text-anchor="middle" fill="#bbbbbb" font-size="12" font-family="sans-serif">AOS 2.4, DOS 1.8</text>

  <text x="20" y="68" text-anchor="start" fill="#dddddd" font-size="13" font-family="sans-serif">High DOS</text>
  <text x="20" y="515" text-anchor="start" fill="#dddddd" font-size="13" font-family="sans-serif">Low DOS</text>
  <text x="150" y="545" text-anchor="middle" fill="#dddddd" font-size="14" font-family="sans-serif">Low AOS</text>
  <text x="580" y="545" text-anchor="middle" fill="#dddddd" font-size="14" font-family="sans-serif">High AOS</text>
</svg>

---

## 혼합 매트릭스 — SAM 버전 (평균 AOS 3.20, DOS 1.93)

<svg width="760" height="600" xmlns="http://www.w3.org/2000/svg">
  <rect x="0" y="0" width="760" height="600" fill="#1b1b1b"/>
  <text x="380" y="35" text-anchor="middle" fill="#f0f0f0" font-size="19" font-family="sans-serif" font-weight="bold">AOS x DOS - SAM - AOS 3.20, DOS 1.93</text>

  <rect x="80" y="60" width="570" height="460" fill="none" stroke="#888888" stroke-width="1.5"/>
  <line x1="365" y1="60" x2="365" y2="520" stroke="#888888" stroke-width="1.5"/>
  <line x1="80" y1="315" x2="650" y2="315" stroke="#888888" stroke-width="1.5"/>

  <text x="222" y="82" text-anchor="middle" fill="#dddddd" font-size="15" font-family="sans-serif">시장 주도</text>
  <text x="507" y="82" text-anchor="middle" fill="#dddddd" font-size="15" font-family="sans-serif">최우선</text>
  <text x="222" y="336" text-anchor="middle" fill="#dddddd" font-size="15" font-family="sans-serif">후순위</text>
  <text x="507" y="336" text-anchor="middle" fill="#dddddd" font-size="15" font-family="sans-serif">니치</text>

  <circle cx="584" cy="131" r="6" fill="#cccccc"/>
  <text x="584" y="118" text-anchor="middle" fill="#f5f5f5" font-size="13" font-family="sans-serif">A 미래지출연결</text>
  <text x="584" y="150" text-anchor="middle" fill="#bbbbbb" font-size="12" font-family="sans-serif">AOS 4.0, DOS 2.8</text>

  <circle cx="365" cy="342" r="6" fill="#cccccc"/>
  <text x="365" y="329" text-anchor="middle" fill="#f5f5f5" font-size="13" font-family="sans-serif">C 실행완주</text>
  <text x="365" y="361" text-anchor="middle" fill="#bbbbbb" font-size="12" font-family="sans-serif">AOS 3.2, DOS 1.8</text>

  <circle cx="146" cy="469" r="6" fill="#cccccc"/>
  <text x="146" y="456" text-anchor="middle" fill="#f5f5f5" font-size="13" font-family="sans-serif">B 신뢰근거</text>
  <text x="146" y="488" text-anchor="middle" fill="#bbbbbb" font-size="12" font-family="sans-serif">AOS 2.4, DOS 1.2</text>

  <text x="20" y="68" text-anchor="start" fill="#dddddd" font-size="13" font-family="sans-serif">High DOS</text>
  <text x="20" y="515" text-anchor="start" fill="#dddddd" font-size="13" font-family="sans-serif">Low DOS</text>
  <text x="150" y="545" text-anchor="middle" fill="#dddddd" font-size="14" font-family="sans-serif">Low AOS</text>
  <text x="580" y="545" text-anchor="middle" fill="#dddddd" font-size="14" font-family="sans-serif">High AOS</text>
</svg>

> 위 SVG가 GitHub에서 렌더링되지 않을 경우를 대비해, 위 "원본 점수" 표가 동일 정보를 담은 대체 형태입니다.

---

## 해석

- **A(미래지출-카드혜택 자동 연결)**: SOM·SAM 두 버전 모두 **최우선**(우상단)에 위치 — AOS·DOS 평균을 모두 넘는 유일한 항목입니다. 모수 선택과 무관한 가장 견고한 1순위입니다.
- **C(실행 완주)**: AOS(3.2)가 정확히 두 버전의 AOS 평균과 같아 경계선 위에 걸칩니다. DOS는 SOM 버전(2.7)·SAM 버전(1.8) 모두 그 버전의 DOS 평균보다 낮아, 두 버전 모두 **니치**(우하단 — 고객 임팩트는 있으나 이번 평균 기준으로는 시장 파급력이 상대적으로 낮게 나옴)로 분류됩니다.
- **B(신뢰 가능한 계산 근거)**: 두 버전 모두 AOS·DOS 평균에 모두 못 미쳐 **후순위**(좌하단)입니다.
- **참고**: 점이 3개뿐이라 평균 자체가 표본에 크게 좌우됩니다 — 특히 C처럼 "중간값"에 해당하는 항목은 평균 경계선 위에 걸리기 쉽습니다. 표본이 늘어나면(D·E·F 등 추가 채점 시) 이 분류는 달라질 수 있습니다.

---

**연결 문서**: `가람/0819_AOS 분석 결과.md` · `가람/0819_DOS 분석 결과.md` · `가람/0819_DOS Market Relevance 모수 판단.md`
