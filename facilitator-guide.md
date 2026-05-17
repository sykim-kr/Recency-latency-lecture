# Recency / Latency 리텐션 분석 방법론 — 내부 분석가 교육 운영안

- Version: v3-final internal analyst workshop
- 대상: 내부 분석가, Product Analytics, CRM Analytics, Growth Analytics 담당자
- 교육 목적: 분석가가 리텐션 문제를 “전체 평균 리포트”가 아니라 고객 행동 시간 구조, 세그먼트, 실험 검증, 수익성 관점으로 진단하고 액션 제안까지 연결하도록 훈련한다.
- 준비물: 슬라이드, 수강자 워크시트 3종, 샘플 이벤트/캠페인 데이터 또는 자사 데이터, 스프레드시트

## 0. 전체 운영 구조 — 3시간

| 시간 | 파트 | 장표 | 분석가 교육 목표 |
|---:|---|---|---|
| 0:00–0:10 | Opening | 01–06 | 후행 지표/전체 평균의 한계 인식 |
| 0:10–0:35 | Recency | 07–15 | 고객 상태 정의와 bucket 설계 역량 |
| 0:35–1:05 | Latency / Tripwire | 16–22 | 반복 행동 시간 구조와 개입 후보 탐지 |
| 1:05–1:15 | Break | - | 휴식 |
| 1:15–1:45 | Cases | 23–31 | 사례를 분석 질문/세그먼트/원인 진단으로 변환 |
| 1:45–2:15 | Reporting & Validation | 32–42 | Mixpanel/BigQuery 리포트와 실험 검증 설계 |
| 2:15–2:50 | Analyst Exercises | 43–50 | 분석 산출물 초안 작성 |
| 2:50–3:00 | Wrap-up | 51–52 | 현업 적용 과제 확정 |

## 1. 내부 분석가 교육 핵심 메시지

1. 분석가는 평균을 보고하는 사람이 아니라 차이를 찾아 의사결정을 바꾸는 사람이다.
2. Recency는 고객의 현재 온도를 정렬하는 변수다.
3. Latency는 고객의 정상 행동 시간표에서 벗어난 순간을 찾는 방법이다.
4. 좋은 분석은 “누가 반응했나”에서 끝나지 않고 “어느 조건에서 돈이 남았나”까지 간다.
5. 리포트 → 인사이트 → 액션 → 실험 → 학습 루프가 만들어져야 분석 방법론이 된다.

## 2. 강의 진행 포인트

### Opening

- 질문: “최근 리텐션/CRM 분석에서 전체 평균 하나로 보고한 적이 있나요?”
- 강조: 평균은 현상을 요약하지만, 액션 대상을 정하지 못한다.

### Recency

- 분석가 과제: 마지막 행동일을 기준으로 고객 상태를 정의한다.
- 주의: 30/60/90일은 정답이 아니라 baseline이다. 반드시 비즈니스 주기와 반응률로 보정한다.

### Latency / Tripwire

- 분석가 과제: 반복 행동 간격을 event_index별로 계산한다.
- 주의: 전체 평균 Latency 하나로 모든 고객을 판단하지 않는다.

### Cases

- Hair Salon: 세그먼트별 정상 주기 차이를 찾는 훈련.
- B2B Software: 재무 문제를 행동 sequence 문제로 번역하는 훈련.
- Discount Ladder: 반응률과 순이익이 다를 때 어떤 KPI를 선택할지 판단하는 훈련.

### Reporting & Validation

- Mixpanel: 분석 질문 → report type → event/breakdown/filter → decision으로 연결.
- BigQuery: raw event log를 user sequence table로 바꾸는 사고 훈련.
- Experiment: control group 없이 campaign effect를 단정하지 않는다.

## 3. 실습 산출물 Definition of Done

각 분석가는 워크숍 종료 시 최소 아래 4개를 작성한다.

1. 핵심 반복 행동 1개와 고객 상태 정의
2. Recency bucket별 분석 테이블 설계
3. Latency sequence / Tripwire 후보 1개
4. Timing × Offer × Profit 실험 설계 초안

## 4. 평가 기준

| 기준 | 좋은 산출물 |
|---|---|
| 질문 명확성 | “무엇을 알고 싶은가”가 의사결정과 연결됨 |
| 세그먼트 | 전체 평균이 아니라 행동/채널/상품/고객군 차이를 봄 |
| 계산 가능성 | 필요한 이벤트/속성/쿼리 구조가 명확함 |
| 액션 연결 | 분석 결과가 CRM/제품/운영 액션으로 이어짐 |
| 검증 계획 | control group, profit KPI, learning이 포함됨 |

## 5. 강의 후 과제

- 1주 내: 실제 데이터로 Recency Distribution 1개 생성
- 2주 내: Response by Recency 또는 Repeat Latency 리포트 1개 생성
- 4주 내: Tripwire 후보와 CRM/제품 액션 제안서 작성
- 6주 내: Control group 포함 실험 설계 리뷰

## 6. 실제 PowerPoint 생성 단계

현재 PPTX는 구조 초안이다. 실제 강의용 PowerPoint는 아래 조건이 충족된 뒤 생성한다.

1. 내부 분석가 교육 목적 반영 완료
2. 강의자 운영안과 워크시트 확정
3. HTML 확인본으로 흐름 검토 완료
4. 표/차트형 장표의 메시지 확정

이후 생성할 파일:

- `recency-latency-retention-methodology-internal-analyst-training-v1.pptx`

생성 후 별도 QA:

- 폰트/여백/표 가독성
- 발표자 노트 포함 여부
- 워크시트 링크/부록 연결
- 3시간 운영안과 장표 번호 일치 여부
