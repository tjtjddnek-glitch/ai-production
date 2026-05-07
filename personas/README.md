# personas — 에이전트 페르소나 14명

이 저장소가 1주기를 돌리는 데 쓰는 페르소나 전부.
사전기획 7명 + 제작(seedance 프롬프트 팀) 7명 = 14명.

---

## 사전기획 7명 (이 폴더 직속)

| 파일 | 역할 | 강점 영역 | Style | Model | Temp |
|---|---|---|---|---|---|
| `researcher.md` | 트렌드 리서처 | 시장·사회 현상 분석, 출처 검증 | 리서치 | (별도) | (별도) |
| `cp_senior.md` | CP (Chief Producer) | 22년차. 평가·토론 주도. 정체성 수호 | 시니어 평가자 | claude-opus-4-7 | 0.6 |
| `pd1_history.md` | PD 1 | 역사·인문. 한국 근현대사·미시사·인물 다큐 | B-목적위임형 | claude-opus-4-7 | 0.75 |
| `pd2_science.md` | PD 2 | 과학·자연. 우주·생물·기후·과학사 | B-목적위임형 | claude-opus-4-7 | 0.75 |
| `pd3_social.md` | PD 3 | 사회·시사·통계. 인구·경제·정책 | B-목적위임형 | claude-opus-4-7 | 0.75 |
| `pd4_global.md` | PD 4 | 글로벌·문화. 비교 인류학·국제 비교 | B-목적위임형 | claude-opus-4-7 | 0.75 |
| `pd5_digital.md` | PD 5 | 디지털·새 포맷. 숏폼-롱폼·메타 콘텐츠 | B-목적위임형 | claude-opus-4-7 | **0.85** |

### 왜 PD가 5명인가

5명 = 한국 지식 콘텐츠 채널의 *최소 도메인 분해* 수.
역사·과학·사회·글로벌·디지털을 동시에 다루는 채널이라면 모든 안건이 5명 중 1명의 강점에 들어온다.
다른 채널은 [docs/ADAPT_TO_YOUR_CHANNEL.md](../docs/ADAPT_TO_YOUR_CHANNEL.md)에서 도메인 분해를 자기 채널에 맞게 갈아끼운다.

### 왜 모두 B-목적위임형인가

3가지 PD 스타일 중 1차 사이클에선 B형으로 통일.
- A: 디테일 명세형 (모든 명세 명시) — Sonnet 4.6, instruction-following
- B: 목적 위임형 (의도·감정 목표만) — **Opus 4.7, 추론·창의 ✓ 1차 사이클**
- C: 반응 협업형 (즉각 피드백 루프) — Sonnet 4.6, temperature 0.9

A·B·C 비교 실험은 다음 사이클에서. 가설 2(워크플로우 = 채용)의 핵심 검증 작업.

### 왜 PD5만 temperature 0.85인가

PD5는 *형식 혁신*이 본업이다. 의외성이 더 필요하다.
PD 1-4는 강점 도메인의 *깊이*가 본업이다. 0.75가 일관성 + 의외성 균형.
CP는 평가자다. 0.6 안정 우선.

→ 자세한 분리 흔적은 [INSIGHTS.md](../INSIGHTS.md) 가설 2.

---

## 제작 7명 (seedance/ 폴더)

컷 콘티 JSON([제-3]) → Seedance 2.0 프롬프트 변환·검수 7인 팀.

| 파일 | 역할 | 무엇을 적는가 |
|---|---|---|
| `seedance/00_prompt_lead.md` | Prompt Lead | 오케스트레이터. 컷 분해 → 위임 → 6단계 포맷으로 조립 |
| `seedance/01_visual_designer.md` | Visual Designer | 피사체·환경·스타일 (프레임 안 무엇이) |
| `seedance/02_cinematographer.md` | Cinematographer | 카메라·라이팅 (어떻게 찍히는가) |
| `seedance/03_motion_director.md` | Motion Director | 액션·시퀀스 (무엇이 일어나는가) |
| `seedance/04_audio_designer.md` | Audio Designer | 대사·SFX·BGM·ambient (네이티브 오디오) |
| `seedance/05_continuity_curator.md` | Continuity Curator | 캐릭터 락·레퍼런스·멀티 컷 일관성 |
| `seedance/06_qc_validator.md` | QC Validator | 생성 전 실패 모드 체크리스트 |

워크플로우:

```
입력: cut_conti_json (한 컷 또는 한 회차 전체)
  │
  ▼
[Prompt Lead]
  ├─ 컷 단위 분해
  ├─ 컷별 specialist 4명에 병렬 위임
  ▼
[Visual] [Cinema] [Motion] [Audio] [Continuity]  ◀── 병렬
  │
  ▼
[Prompt Lead] 6단계 포맷으로 조립 (60-100 단어)
  │
  ▼
[QC Validator] 실패 모드 체크
  ├─ pass → 출력
  └─ fail → Lead가 해당 specialist에게 재요청 (최대 2회)
  │
  ▼
출력: { cut_id, seedance_prompt, ... }
```

자세한 워크플로우·6단계 포맷·실패 모드 체크리스트는 `seedance/README.md`.

### Seedance 2.0 (2026-05 기준)

| 항목 | 값 |
|---|---|
| 접근 경로 | Runway Unlimited 플랜 ($76-95/월, 무제한) |
| 단일 클립 길이 | 4-15초 (paid), 12초 (Lite) |
| 권장 프롬프트 | 60-100 단어, 영어 |
| 프롬프트 구조 | Subject → Action → Environment → Camera → Lighting → Style |
| 네거티브 프롬프트 | **미지원** ("--no", "without" 무시) |
| 네이티브 오디오 | 단일 패스로 dialogue/SFX/BGM/ambient 동시 생성 |
| 립싱크 언어 | 8+ (한국어 포함, 짧은 문장에서만 안정) |
| 멀티 컷 | `[00:00-00:05]` 타임스탬프로 분기 가능 |
| 캐릭터 락 | `@Character1`, `@Image1` + 레퍼런스 이미지 |

#### 알려진 실패 모드 (콘티 단계에서 미리 차단)

- **글자 → 글립 수프**: 표지판·자막·티셔츠 문구 못 읽음. 화면 안 텍스트 X.
- **손가락 드리프트**: 익스트림 클로즈업에서 손가락 늘어남·꺾임·합체. 미디엄 이상 거리.
- **빠른 모션 워핑**: "fast" 키워드는 화질 저하 1순위. "smooth/measured/slow".
- **거울·반사 물리 깨짐**: 반사 컷 피하기.
- **한국어 립싱크 드리프트**: 10단어 넘는 대사에서 어긋남. 짧게 쪼개기.
- **카메라+피사체 동시 빠른 이동**: 흔들림. 한쪽만 빠르게.

→ 이 실패 모드들이 *콘티 단계 [제-3]에서 negative prompt로 명시*된다. 가설 1(컷-레벨 디렉터)의 직접 증거.

---

## 페르소나 14명의 모델·온도 분포

```
Opus 4.7 / 0.6   1명  cp_senior
Opus 4.7 / 0.75  4명  pd1, pd2, pd3, pd4
Opus 4.7 / 0.85  1명  pd5
(별도)            1명  researcher
seedance 7명     —    호출자가 모델 지정 (Lead는 Opus, Validator는 Sonnet 권장)
```

### 다음 사이클 실험 후보

- [ ] PD 페르소나의 *모델* 차이 분리 (지금은 모두 Opus). Sonnet 4.6 vs Opus 4.7.
- [ ] PD 페르소나의 *Style* 차이 (지금은 모두 B). A·C와의 비교.
- [ ] CP 페르소나 복수화 (지금은 1명). 시니어 CP + 사실 검증 강성 CP + 영상 톤 CP + 편집 CP — 회의 006의 CP 4명 분리 실험과 같음.

---

## 받아쓸 때 손대는 우선순위

자기 채널·도메인으로 옮길 때:

1. **먼저** `cp_senior.md`의 5축 평가 기준 — 이게 채널 정체성의 핵심.
2. **그다음** `pd1~5_*.md`의 *강점 영역*과 *좋아하는 작가·레퍼런스* — PD가 진짜 다르게 작동하게 만드는 부분.
3. **그다음** `researcher.md`의 *트렌드 소스* — 자기 도메인의 공식·비공식 출처.
4. **선택** `seedance/` — 영상 생성하지 않으면 무시.

자세한 가이드는 [docs/ADAPT_TO_YOUR_CHANNEL.md](../docs/ADAPT_TO_YOUR_CHANNEL.md).
