---
team_id: seedance_prompt_team
purpose: 컷 콘티 JSON([제-3]) → Runway Unlimited의 Seedance 2.0 프롬프트로 변환
target_model: Seedance 2.0 (via Runway Unlimited)
created: 2026-05-04
---

# Seedance 2.0 프롬프트 작성 팀

## 한 줄 요약
[제-3] 컷 콘티 JSON을 받아 Runway Unlimited의 Seedance 2.0이 가장 잘 알아먹는 60-100 단어 영어 프롬프트로 번역하고 검수하는 6+1인 전문가 팀.

---

## 모델 팩트 (2026-05 기준)

| 항목 | 값 |
|---|---|
| 접근 경로 | Runway Unlimited 플랜 ($76-95/월, 무제한 생성) |
| 단일 클립 길이 | 4-15초 (paid), 12초 (Lite) |
| 권장 프롬프트 길이 | 60-100 단어, 영어 |
| 프롬프트 구조 | Subject → Action → Environment → Camera → Lighting → Style (6단계) |
| 네거티브 프롬프트 | **미지원** ("--no", "without" 류 무시됨) |
| 네이티브 오디오 | 단일 패스로 dialogue/SFX/BGM/ambient 동시 생성 |
| 립싱크 언어 | 8+ 언어 (한국어 포함) — 한국어는 짧은 문장에서만 안정 |
| 멀티 컷 | 단일 생성 안에서 `[00:00-00:05]` 타임스탬프로 컷 분기 가능 |
| 캐릭터 락 | `@Character1`, `@Image1` 태그 + 레퍼런스 이미지 |

## 알려진 실패 모드

- **글자 → 글립 수프**: 표지판·자막·티셔츠 문구 못 읽음. 한글이든 영문이든 화면 안 텍스트 X.
- **손가락 드리프트**: 익스트림 클로즈업에서 손가락 늘어남·꺾임·합체. 미디엄 이상 거리로 프레이밍.
- **빠른 모션 워핑**: "fast" 키워드는 화질 저하 1순위. "smooth/measured/slow" 지향.
- **거울·반사 물리 깨짐**: 거울 안 인물 비대칭. 반사 컷 피하기.
- **한국어 립싱크 드리프트**: 10단어 넘는 대사에서 어긋남. 짧게 쪼개기.
- **카메라+피사체 동시 빠른 이동**: 흔들림·왜곡. 한쪽만 빠르게.

---

## 팀 구성

```
[Prompt Lead]                    오케스트레이터 — 입력 파싱·위임·조립·재시도
    │
    ├─ [Visual Designer]         피사체·환경·스타일 (프레임 안에 무엇이)
    ├─ [Cinematographer]         카메라·라이팅 (어떻게 찍히는가)
    ├─ [Motion Director]         액션·시퀀스 (무엇이 일어나는가)
    ├─ [Audio Designer]          대사·SFX·BGM·ambient (네이티브 오디오)
    └─ [Continuity Curator]      캐릭터 락·레퍼런스·멀티 컷 일관성
    │
[QC Validator]                   생성 전 실패 모드 체크리스트
```

## 워크플로우

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
[QC Validator] 실패모드 체크
  ├─ pass → 출력
  └─ fail → Lead가 해당 specialist에게 재요청 (최대 2회)
  │
  ▼
출력: { cut_id, seedance_prompt, duration_sec, priority, must_have, fallback_tier, reroll_budget, reference_images[], qc_status, qc_notes }
```

## 6단계 프롬프트 템플릿 (Lead 조립용)

```
[Subject] one primary subject, distinctive identifying details.
[Action] one primary visible action; if sequenced, use "then / followed by".
[Environment] location, time of day, weather, key background details.
[Camera] one camera move (push / pull / pan / track / orbit / follow / crane / zoom),
         pacing word (slow/smooth/gentle).
[Lighting] one mood line (warm afternoon side light / cool overcast / neon backlit ...).
[Style] genre + render reference (cinematic documentary / hand-held vérité / film grain ...).
[+ Audio block] "<dialogue line>" + ambient/SFX list + BGM mood.
[+ Reference tag] @Character1 / @Image1 + consistency clause if multi-shot or recurring.
```

## 멀티 컷 타임스탬프 패턴 (한 생성 안에서)

```
[00:00-00:03] establishing shot of ...
[00:03-00:08] medium close-up, character speaks "..."
[00:08-00:12] cutaway to ...
```

EBS 다큐는 4-15초 단일 컷으로 끊는 게 안정적. 멀티 컷은 인터뷰+B롤 묶음 같이 명확히 다른 앵글일 때만.

---

## 출력 스키마 (Lead 최종)

```json
{
  "cut_id": "ep01_c003",
  "duration_sec": 8,
  "priority": 1,
  "must_have": true,
  "fallback_tier": "none",
  "reroll_budget": 2,
  "seedance_prompt": "A 1973 Seoul seamstress girl, 14, threadbare uniform, pulls a heavy fabric bundle through narrow Cheonggyecheon market alley. Steam rises from sewing machines on either side. Late afternoon, golden hour, dusty air. Camera tracks slowly behind her at hip height. Warm tungsten light bleeds from open shop doors, deep blue shadows in the alley. Documentary handheld, film grain, archival reconstruction tone. Ambient: distant pedal sewing machines, muffled radio. No dialogue.",
  "reference_images": ["assets/refs/cheonggyecheon_1973.jpg"],
  "character_refs": ["@Character_seamstress01"],
  "qc_status": "pass",
  "qc_notes": "78 words. No on-frame text. No close-up hands. Single camera move. Korean dialogue absent — safe.",
  "issued_at": "2026-05-04"
}
```

## Runway 큐 운영 메타데이터

Runway Unlimited/Explore에서 동시에 2개만 생성할 수 있으므로, Lead는 프롬프트와 함께 큐 운영 필드를 반드시 붙인다.

| 필드 | 값 | 기준 |
|---|---|---|
| `priority` | 1-5 | 1은 훅·결론·핵심 증거 컷, 5는 남는 시간용 실험 컷 |
| `must_have` | boolean | 쇼츠 60초 구조상 빠지면 안 되는 컷인지 |
| `fallback_tier` | `none` / `kling_ok` / `stock_ok` / `edit_only` | Seedance 실패·대기 시 대체 경로 |
| `reroll_budget` | 0-3 | 마감 전 허용할 최대 재생성 횟수 |

권장 기본값:

- 훅/결론/과학적 증거 컷: `priority=1`, `must_have=true`, `fallback_tier=none`, `reroll_budget=2`
- 주요 재현/상징 컷: `priority=2`, `must_have=true`, `fallback_tier=kling_ok`, `reroll_budget=1`
- 분위기 B-roll: `priority=3`, `must_have=false`, `fallback_tier=stock_ok`, `reroll_budget=1`
- 자막·그래픽으로 대체 가능한 컷: `priority=4`, `must_have=false`, `fallback_tier=edit_only`, `reroll_budget=0`

---

## EBS 톤 가드레일 (전 specialist 공통)

- "AI로 더 빠르게" 톤 X / **"AI로 더 깊게"** O — 사료 복원·시간 압축·시뮬레이션 같은 본질적 활용.
- 광고·예능 톤 X. 다큐·교양 호흡.
- 자극적 클로즈업·과장 카메라 무빙 X. 절제된 한국 다큐 톤.
- 재현 영상에는 "archival reconstruction" / "documentary reconstruction" 명시 (메타데이터로도 남김).
- 인물 미화·왜곡 금지. 시대·신체·복식 고증.

## 외부 참고 (2026-05 검색)

- Runway Unlimited + Seedance 2.0: https://help.runwayml.com/hc/en-us/articles/50488490233363
- 6단계 공식 가이드: https://help.apiyi.com/en/seedance-2-0-prompt-guide-video-generation-camera-style-tips-en.html
- 오디오 가이드: https://www.cutout.pro/learn/blog-seedance-2-0-audio-guide/
- 일관성·멀티 컷: https://higgsfield.ai/blog/seedance-prompting-guide
- 한계·실패 모드: https://videoai.me/blog/seedance-2-0-limitations
- 스킬 구조 영감: https://github.com/Emily2040/seedance-2.0

---

*Living document. Seedance·Runway 정책 변경 시 즉시 업데이트.*
