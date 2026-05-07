# GETTING_STARTED.md — 자기 채널에 적용하는 5단계

이 저장소는 *다시본다 / 한국의 시계* 채널을 위한 1차 사이클 케이스를 담고 있다.
받아쓰는 사람은 페르소나의 정체성·평가 기준·강점 영역만 자기 채널에 맞게 갈아끼우면 된다.

목표 시간: **반나절** (페르소나 커스터마이즈 + 첫 사이클 1단계까지).

---

## 0. 받아쓰기 전 점검

이 시스템이 자기 채널에 맞는지 5분 점검.

**맞는 경우**:
- 채널이 *지식·교양·다큐* 결이다 (밈·바이럴 X)
- 1편 만드는 데 기획·검증·콘티 단계가 길다
- 사실 검증·고증이 필요하다 (역사·과학·시사·문화)
- 한 사람이 처리하기엔 검토 관점이 너무 많다

**안 맞는 경우**:
- 채널이 *반응 속도*가 본업이다 (뉴스 속보·트렌드 픽업)
- 라이브·즉흥·인터뷰가 핵심이다
- 한 사람의 강한 톤이 채널 정체성이다 (페르소나 분리가 오히려 약화)

---

## Step 1 — 채널 정체성 한 줄 정의

### 무엇을 적는가

```
채널 이름:        ___________
한 줄 소개:       시청자가 ____를 ____하게 보게 한다
시즌 단위:        ___분 × ___부작
진입 단위:        ___초 입구 영상 (60초 또는 90초 권장)
```

`다시본다`의 경우:
- 채널 이름: 다시본다
- 한 줄 소개: *시청자가 한국 현실을 다시 보게 한다*
- 시즌 단위: 20분 × 8부작
- 진입 단위: 3분(180초) × 12컷 — 더 짧게도 가능

### 어디에 적는가

```
case-studies/your-channel-cycle-001/00_channel_identity.md
```

이 한 줄이 모든 페르소나의 평가 기준의 상위 가치가 된다. CP가 5축 점수 매길 때, 이 한 줄에 안 맞으면 *왜 이 채널인가* 답이 안 된다.

---

## Step 2 — 페르소나 커스터마이즈

```bash
cp -R personas/ case-studies/your-channel-cycle-001/personas/
```

### CP 페르소나 (`personas/cp_senior.md`)

가장 먼저 손대는 곳. 5축 평가 기준이 채널 정체성의 핵심이다.

EBS 버전:
1. 공공성·공교양
2. 고증·신뢰성
3. 학습 의도성
4. 확장성·아카이브성
5. AI 활용의 필연성

자기 채널 버전 예시 (시사 채널이면):
1. 시의성
2. 사실 검증
3. 다각도 관점
4. 한국 시청자 직격
5. AI 활용의 필연성

→ 5축이 채널 정체성을 정확히 반영하는지 점검. 약하면 1차 사이클부터 결이 흐려진다.

### PD 페르소나 5명

5명 모두 *강점 영역*이 다르다. 자기 채널의 도메인을 분해.

EBS 버전 (5명):
- pd1_history (역사·인문)
- pd2_science (과학·자연)
- pd3_social (사회·시사·통계)
- pd4_global (글로벌·문화)
- pd5_digital (디지털·새 포맷)

자기 채널 버전 예시:
- **테크 채널**: pd1_hardware / pd2_ai / pd3_developer / pd4_business / pd5_culture
- **건강 채널**: pd1_clinical / pd2_nutrition / pd3_mental / pd4_policy / pd5_lifestyle
- **요리 채널**: pd1_history / pd2_chemistry / pd3_global / pd4_home / pd5_format

각 PD의 system prompt에서 갈아낄 부분:
- 강점 영역 (분야)
- 사고 스타일 (어떻게 안건을 떠올리는가)
- 좋아하는 톤·작가·채널 레퍼런스
- temperature (디지털·새포맷 PD만 0.85, 나머지는 0.75)

### researcher 페르소나

채널 정체성에 맞는 트렌드 소스 정의.
EBS 버전은 학술 논문·통계청·한국학중앙연구원 등 공식 출처 우선.
자기 채널은 자기 도메인의 *공식 vs 비공식* 출처를 어떻게 섞을지 정하기.

### seedance 7인 팀 (선택)

영상 생성을 한다면 그대로 사용 가능. 영상 생성을 안 하면 무시해도 됨.

---

## Step 3 — 트렌드 리서치 입력 준비

```
case-studies/your-channel-cycle-001/01_research.json
```

researcher 페르소나가 산출하는 형식.

```json
{
  "research_id": "cycle-001-research",
  "queries": ["..."],
  "findings": [
    { "topic": "...", "summary": "...", "sources": ["url1"], "relevance_score": 0.85 }
  ],
  "trend_signals": ["..."],
  "blind_spots": ["..."]
}
```

수동 입력해도 됨. 자기가 찾은 트렌드 자료를 이 형식으로 정리.

---

## Step 4 — PD 5명 × 6 = 30개 로그라인 돌리기

각 PD에게 같은 트렌드 리서치를 주고 6개씩 산출 요청.

```
입력: 01_research.json + 페르소나 정의
출력: 02_pd1_loglines.json ~ 02_pd5_loglines.json
```

각 로그라인 1개당:

```json
{
  "logline_id": "pd2-5",
  "pd_persona": "pd2_science",
  "logline": "한 줄",
  "research_summary": "...",
  "why_good": "...",
  "sources": ["url1", "url2"],
  "ai_necessity": "AI 아니면 불가능한 이유",
  "ebs_fit_score": 0-10,
  "novelty_score": 0-10
}
```

→ 5 PD가 *명확히 다른 결*의 로그라인을 내야 페르소나 분리가 작동 중. 결이 비슷하면 system prompt가 약함.

---

## Step 5 — 인간 컷 [2] 첫 개입

CP 페르소나에게 30개 로그라인을 주고 5축 점수 매기게 한다.

```
입력: 30개 로그라인 + CP 페르소나
출력: 03_cp_evaluation.json
```

그다음 사용자가 *PD별 1개씩* 5개 픽.

```json
{
  "human_cut_id": "pd-1to5",
  "selected_loglines": ["pd1-3", "pd2-5", "pd3-5", "pd4-1", "pd5-1"],
  "rationale": "..."
}
```

→ 인간 개입의 첫 지점. 자세한 가이드는 [HUMAN_INTERVENTION.md](./HUMAN_INTERVENTION.md).

여기까지가 반나절. 이후 [3] 디벨롭 → [4] 발표회 → [5] 픽 → [6] 전사회의 → 제작 트랙은 [PIPELINE.md](../PIPELINE.md) 참고.

---

## 자주 막히는 곳

### "PD 5명이 다 비슷한 결의 로그라인을 낸다"

→ system prompt에서 *강점 영역*만 다르고 *사고 스타일·톤·레퍼런스*가 같으면 결이 비슷해진다. 다음을 갈아낀다.
- 좋아하는 작가·채널·다큐 레퍼런스 (PD별로 다른 작가)
- "어떻게 안건을 떠올리는가" 한 문단 (PD별로 다른 사고 스타일)
- 무엇을 *피하는가* (PD별 NG 결)

### "CP가 모든 안건을 비슷한 점수로 매긴다"

→ 5축 평가 기준이 채널 정체성을 충분히 분리하지 못함. 5축 중 *가장 채널다움을 결정하는 1축*에 가중치를 더 높게.

### "사실 검증이 너무 늦게 발견된다"

→ 1차 사이클 회의 003 → 004의 *1936 잉크 멀티스펙트럼* 폐기 사건과 같음. **사실 검증을 콘티 단계 [제-3] 전에 명시 단계로 끼우기**. 학술 논문·통계 출처 0건이면 콘티 단계 진입 차단.

→ [DECISIONS.md](../DECISIONS.md) 결정 14·15 참고.

### "인간 개입이 너무 많아서 시뮬레이션 의미가 없다"

→ 인간 개입 4곳 ([2], [5], [8], [제-6])이 정해진 양이다. 이 4곳 외에서 자꾸 사람이 끼어들면 시뮬레이션이 아니라 보조 도구가 됨. 4곳에서만 결정하고 나머지는 페르소나에 맡기는 *위임 훈련*이 PD 본업.

→ [HUMAN_INTERVENTION.md](./HUMAN_INTERVENTION.md)에서 각 지점에서 무엇을 봐야 하는지 디테일.

---

## 1차 사이클 끝나면

```
case-studies/your-channel-cycle-001/
├── 00_channel_identity.md
├── 01_research.json
├── 02_pd1_loglines.json ~ 02_pd5_loglines.json
├── 03_cp_evaluation.json
├── 04_human_cut.json
├── 04_pd*_develop.json
├── conference_*.md (발표회 + 전사회의)
├── 05_final_pick.json
├── episode_001_*.md (12컷 콘티)
└── outputs/ (영상 생성 결과)
```

이 폴더 자체가 *받아쓰는 사람의 1차 사이클 증거*다.
다른 채널의 사이클이 늘어나면 이 저장소의 `case-studies/`에 풀리퀘로 합칠 수 있음.

---

## 다음 단계

- 다른 채널·도메인으로 페르소나 커스터마이즈: [ADAPT_TO_YOUR_CHANNEL.md](./ADAPT_TO_YOUR_CHANNEL.md)
- 인간 개입 4곳 디테일: [HUMAN_INTERVENTION.md](./HUMAN_INTERVENTION.md)
- 메타 가설 2개 검증 흔적: [../INSIGHTS.md](../INSIGHTS.md)
