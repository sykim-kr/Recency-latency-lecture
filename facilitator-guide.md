# Recency / Latency 리텐션 분석 & CRM 자동화 — 3시간 워크숍 운영안

- Version: v3-final full workshop
- 대상: CRM, Growth, Product Analytics, Marketing 실무자
- 운영 목표: 참가자가 자사 데이터로 Recency bucket, Latency sequence, Tripwire, Timing × Offer × Profit 실험을 설계할 수 있게 만든다.
- 준비물: 슬라이드, 수강자 워크시트 3종, 샘플 데이터 또는 자사 이벤트/캠페인 데이터, 계산기/스프레드시트

## 0. 전체 운영 구조

| 시간 | 파트 | 장표 | 목표 |
|---:|---|---|---|
| 0:00–0:10 | Opening | 01–06 | 왜 평균/후행지표만 보면 늦는지 문제의식 형성 |
| 0:10–0:35 | Recency | 07–15 | 고객 상태 정의와 Recency bucket 설계 |
| 0:35–1:05 | Latency / Tripwire | 16–22 | 정상 행동 시간표와 개입 후보 찾기 |
| 1:05–1:15 | Break | - | 휴식 |
| 1:15–1:45 | Cases | 23–31 | Hair Salon/B2B/Offer 사례로 원리 이해 |
| 1:45–2:15 | Reporting & Automation | 32–42 | Mixpanel/BigQuery/CRM Journey 설계 |
| 2:15–2:50 | Exercises | 43–50 | 워크시트 3종 작성 |
| 2:50–3:00 | Wrap-up | 51–52 | 체크리스트와 팀 적용 액션 확정 |

## 1. 강의자 핵심 메시지

1. 이탈은 사건이 아니라 고객 LifeCycle의 마찰 변화다.
2. 전체 평균은 보고용이고, 세그먼트는 액션용이다.
3. Recency는 반응 가능성을 정렬하고, Latency는 개입 타이밍을 알려준다.
4. CRM 실험의 목표는 클릭률/반응률이 아니라 순이익이다.
5. 자동화는 발송 룰이 아니라 반복 학습 시스템이다.

## 2. 장표별 진행 메모

### SLIDE 01–06 Opening

- 질문: “우리 팀은 고객이 떠나는 걸 언제 알게 되나요?”
- 강조: 월매출/전체 활성/전체 반응률은 대부분 후행 지표다.
- 운영 팁: 초반부터 AI/ML 예측으로 가지 말고, “마지막 행동 이후 시간”이라는 단순한 출발점을 잡는다.

### SLIDE 07–15 Recency

- 질문: “우리 서비스에서 마지막 의미 있는 행동은 무엇인가?”
- 강조: 30-60-90 bucket은 정답이 아니라 시작점이다.
- 실습 연결: Worksheet 1 작성 준비.

### SLIDE 16–22 Latency / Tripwire

- 질문: “고객이 원래 돌아와야 할 정상 주기를 알고 있나요?”
- 강조: 모든 고객에게 같은 threshold를 쓰면 이른 할인과 늦은 win-back이 동시에 생긴다.
- 실습 연결: Worksheet 2 작성 준비.

### SLIDE 23–31 Cases & Profit

- Hair Salon: 메시지가 아니라 타이밍 문제.
- B2B Software: 재무 문제를 행동 interval 문제로 번역.
- Discount Ladder: 반응률 winner와 profit winner가 다를 수 있음.
- 질문: “우리 팀 KPI는 response winner를 뽑나요, profit winner를 뽑나요?”

### SLIDE 32–42 Reporting / Automation

- Mixpanel 4대 리포트: Distribution, Response, Tripwire, Milestone Latency.
- BigQuery: raw event log → sequence table → bucket profit table.
- CRM Journey: Trigger / Segment / Timing / Offer / Measurement.

### SLIDE 43–50 Exercises

- 3개 워크시트를 모두 완성하지 못해도 됨.
- 최소 산출물: 핵심 행동 1개, Recency bucket 3개, Tripwire 후보 1개, Offer test 1개.

### SLIDE 51–52 Wrap-up

- 팀별로 “이번 주 할 일 1개”를 말하게 한다.
- 강의 후 액션: 캠페인 리포트에 Recency bucket별 반응률 추가.

## 3. 진행자 질문 Bank

- 우리 고객은 어느 날 갑자기 떠나나요, 아니면 먼저 행동 간격이 길어지나요?
- 현재 리포트에서 전체 평균이 숨기고 있는 차이는 무엇인가요?
- 우리 비즈니스의 “long cut / short cut” 세그먼트는 무엇인가요?
- 지금 CRM은 너무 이른 할인과 너무 늦은 win-back 중 어디에 더 가까운가요?
- 경영진에게 보여줄 KPI는 클릭률인가, 순이익인가?

## 4. 준비 체크리스트

- [ ] 핵심 행동 이벤트 1개 선정
- [ ] 마지막 행동일 또는 이벤트 로그 준비
- [ ] 캠페인 발송/반응/구매/매출/마진 데이터 준비
- [ ] 워크시트 3종 배포
- [ ] 실습 결과 공유 방식 결정

## 5. 강의 후 Follow-up

- 1주 내: Recency Distribution 리포트 생성
- 2주 내: Response by Recency 리포트 생성
- 4주 내: Timing × Offer 실험 1개 실행
- 6주 내: Control group 포함 incremental profit 리뷰
