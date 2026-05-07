# 09. 영상 출력물 — Seedance 2.0 mp4 매핑 표 + YouTube 게시 4편

> 실제 mp4 파일은 git 미포함(용량). 이 README는 *어떤 prompt가 어떤 mp4를 만들었는가*의 매핑 표.
> 콘티(`08_storyboards/`)와 출력(이 폴더)을 한 화살표로 연결한다.
> **이 사이클의 진짜 마침표**: 4편이 YouTube `@dasibonda`에 실제 게시됨.

---

## ★ YouTube @dasibonda 게시 4편

| # | YouTube | 컨셉 | 페르소나 | 콘티 위치 |
|---|---|---|---|---|
| 1 | [shorts/1DU3Ciia_zw](https://www.youtube.com/shorts/1DU3Ciia_zw) | 별자리 1438 | PD2 과학 | (sync 후 정확 위치 / 현재 `runs/cycle-001/v5_60sec/conference_002.md` 또는 `04_pd2-5.json` 압축본 추정) |
| 2 | [shorts/VKzCareMI4Q](https://www.youtube.com/shorts/VKzCareMI4Q) | 식자공 1936 | PD1 역사 | `07_conference_evolution/shorts_pd1.md` (8컷 콘티) |
| 3 | [shorts/an6yJBIoBG0](https://www.youtube.com/shorts/an6yJBIoBG0) | 의병 invisible_mountain | PD1 역사 | `runs/cycle-001/v5_60sec/shorts_pd1.md` (부분) + `05_developed/04_pd1-5.json` |
| 4 | [shorts/GPUglXi4o4c](https://www.youtube.com/shorts/GPUglXi4o4c) | 점심값 lunch10000 | PD3 사회 | `07_conference_evolution/shorts_pd3.md` |

→ 4편 모두 60초 입구. *"다시본다" 채널 정체성의 첫 시각 증거*.

**sync 안내**: ssh seoseong-u@macbook-pro-2 자료가 곧 sync 예정. sync 후 별자리 1438 / 점심값 lunch10000의 정확한 콘티 위치가 갱신될 수 있음. 현재는 추정 위치만.

---

## ★ 페르소나별 채택률 (현재까지) — 메타 가설 2 자연 데이터

| 페르소나 | 등장 | 로그라인 6 | 인간 픽 | 디벨롭 | 60초 콘티 | YouTube 게시 |
|---|---|---|---|---|---|---|
| **PD1 역사덕후** | cycle 시작 | 6 | 1 (PD1-5) | 1 | 1 (`shorts_pd1.md`) + invisible_mountain 60초 콘티 GAP | **2** ★ (식자공·의병) |
| **PD2 과학덕후** | cycle 시작 | 6 | 1 (PD2-5) | 1 | **콘티 GAP — `shorts_pd2.md` 부재** (v4 7분만) | **1** (별자리 1438, sync 대기) |
| **PD3 사회덕후** | cycle 시작 | 6 | 3 (PD3-1·5·6) | 3 | 1 (`shorts_pd3.md`) | **1** (점심값, sync 대기) |
| **PD4 글로벌덕후** | cycle 시작 | 6 | 1 (PD4-1) | 1 | 1 (`shorts_pd4.md`) | 0 (콘티 있지만 미게시) |
| **PD5 디지털덕후** | cycle 시작 | 6 | 1 (PD5-1) | 1 | 1 (`shorts_pd5.md`, 광공해) | 0 (콘티 있지만 미게시) |
| **PD6 김진혁 결** | **conference_005 자연 발생** | — | — | — | (33초·반도체 콘티 회의록 안에 박힘) | 0 |
| **총** | — | **30** | **7** | **7** | **5+ GAP 2건** | **4** |

### 채택률 해석

- **PD1 역사덕후 50% (2/4편 채택)** — 미시사·작은 사물 결이 60초 입구 포맷에 가장 잘 맞음. 식자공의 핀셋 90초 / 의병이 못 본 17일 — 둘 다 *작은 한 점에서 큰 시간으로 시청자를 이동*시키는 1438별 결의 변형.
- **PD2 과학덕후 25% (1/4편)** — 1438별의 결과 중심 천문. 단 콘티 GAP(`shorts_pd2.md` 부재) — 7분 콘티에서 60초로 *건너뛰기 운영*한 흔적.
- **PD3 사회덕후 25% (1/4편)** — 인간이 가장 많이 픽했지만(3개) 60초 압축 적합도는 1편만. 정책 회귀(PD3-6)·골목 25년(PD3-1)은 60초로 압축 불가.
- **PD4·PD5 0% (0/4편)** — 글로벌 비교(PD4)·메타 다큐(PD5)는 *콘티는 있지만* 60초로 영상 생성·게시까지 도달 못 함. 두 페르소나 모두 60초 입구로는 *결이 못 살아남*. 시즌 단위 묶음으로 흡수 필요.
- **PD6 김진혁 결 — 워크플로우 진행 중 자연 발생**: cycle 시작 시 5명 페르소나였다. conference_005에서 *마음 직격이 약하다*는 사용자 피드백 후 PD6이 회의에 추가 — 즉 **워크플로우가 사이클 한복판에서 새 페르소나를 *채용*했다**. 게시 0편이지만 33초·반도체 회의록 안에 컨셉이 박혀있고, 다음 사이클의 정식 6번째 페르소나로 등록 필요.

→ **결론**: 페르소나마다 *60초 입구 적합도*가 다르다. PD1·PD2·PD3은 60초 채널 입구에, PD4·PD5는 시즌 단위 다큐에 더 적합. PD6은 *결의 보강용으로 채용된 임시 페르소나*. 이게 *"운영 = 정해진 워크플로우"* 단계의 첫 운영 데이터 — 다음 사이클 페르소나 system prompt에 *60초 압축 적합 결*과 *시즌 길이 결*을 분리 명시할 수 있음.

→ **신호 한 줄**: PD1 역사덕후가 현재까지 채택률 1위(2/4편)라는 사실은 *이 시점 채널의 결이 역사 쪽으로 결정되고 있다*는 의미. "다시본다" 채널의 첫 정체성은 결국 *한국 미시사 + 작은 사물 → 큰 시간*의 결이 됐다. 이게 가설 2(워크플로우=채용)의 첫 자연 발생 데이터 — 워크플로우를 운영하면 *어느 페르소나의 결이 채널 정체성으로 굳어질지*가 자연스럽게 결정된다.

### 다음 사이클 액션 시그널

1. **PD1 역사덕후 system prompt 강화** — 미시사·작은 사물 결을 *기본 출력 결*로 명시. 60초 입구 누적의 핵심 페르소나로 운용.
2. **PD4·PD5는 시즌 트랙 분리** — 60초 단발 시도 X, 처음부터 시즌형 4부작 단위로 페르소나 운용.
3. **PD6 김진혁 결 정식 채용** — 005 회의에서 자연 발생한 임시 페르소나를 system-prompt 단계에서 분리 작성. 메타 가설 2의 두 번째 분기 데이터의 정식화.
4. **6번째 평가 축 "시리즈 일관성·테마 묶기"** — 인간 픽이 자연 발생적으로 보여준 결을 CP 평가에 추가 (Conf 002~006의 누적 룰과 동조).
5. **콘티 GAP 채우기** — 1438별 60초 콘티(`shorts_pd2.md`) 작성 + invisible_mountain 60초 콘티 작성. *콘티 없이 운영된 흔적*은 다음 사이클에서 표준화 도구로 흡수.

---

## 단계 위치

```
[8] 콘티
[9] 영상 출력 ★  ← 이 단계
[10] 사이트 (별도 세션)
```

---

## 영상 출력 위치 (원본)

`/Users/seulchankim/projects/personal/aipd/runs/cycle-001/v5_60sec/outputs/`

```
outputs/
├── _unsorted/                      # 5/5 초기 톤 테스트 2건
├── ep_pd1_invisible_mountain/      # PD1-5 보이지 않는 산 (로컬 8개, 채널 게시)
├── ep_pd1_typesetter1936/          # PD1 식자공 1936 (로컬 10개, 채널 게시)
├── ep_pd2_5_stars1438/             # PD2-5 1438년 별 (로컬 0개 — mbp2 sync 대기, 채널 게시)
├── ep_pd3_lunch10000/              # PD3 점심값 (로컬 0개 — mbp2 sync 대기, 채널 게시)
└── ep_pd4_1903photo/               # PD4 1903년 사진 (로컬 0개, 채널 미게시 — 콘티만)
```

→ **로컬 mp4: 20개** (invisible_mountain 8 + typesetter1936 10 + unsorted 2). 1438·점심값은 원격 환경에서 작업 중 — rsync 후 stars1438·lunch10000 폴더가 채워질 예정.

---

## 매핑 표 — ep_pd1_typesetter1936 (식자공 1936, 10개) — YouTube 게시됨

콘티 원본: `runs/cycle-001/v5_60sec/shorts_pd1.md` (60초 8컷)

이 콘티는 *동아일보 1936년 일장기 말소 사건*의 식자공 시점. Conference 003의 "1936년 잉크 세 번"이 콘티 단계 픽션으로 폐기됐을 때, *원형*은 살아남았다 — `shorts_pd1.md`의 식자공의 핀셋 90초는 멀티스펙트럼 픽션 없이 *작업대 위 한 손*에 시선을 둔 미시사 결.

| # | 콘티 컷 | duration | style 키워드 | mp4 파일명 (Style 발췌) | 크기 |
|---|---|---|---|---|---|
| C01 | CUT 01 - 활자함 슬라이드 | 8s | Documentary archival reconstruction | `Documentary archiv.mp4` | 2.0MB |
| C02 | CUT 02 - 사진 위 손가락 두 번 탭 | 7s | Same archival reconstruction tone | `Same archival reco.mp4` | 1.8MB |
| C03 | CUT 03 - 두 실루엣 (기자·식자공) | 7s | Documentary reconstruction, side profile silhouette | `Documentary recons.mp4` | 1.5MB |
| C04 | CUT 04 - 핀셋이 활자 두 개 빼냄 | 8s | Macro documentary, slow tactile motion | `Macro documentary_.mp4` | 2.3MB |
| C05 | CUT 05 - 잉크 → 종이 → 빈 가슴 | 7s | Macro tactile reconstruction, ink texture | `Macro tactile reco.mp4` | 2.3MB |
| C06 | CUT 06 - 정간 명령 도장 | 7s | Archival document overlay style | `Archival document.mp4` | 2.1MB |
| C07 | CUT 07 - 시간 경과 + PIP 매크로 | 8s | Time-lapse style still composition | `Time-lapse style s.mp4` 원본 + `_160733` + `_160748` | 1.8MB |
| C08 | CUT 08 - 빈 활자 두 개 클로즈업 | 8s | Final still card composition | `Final still card c.mp4` | 1.9MB |

**총 10개 = 8컷 + 시간경과(C07) 재생성 2회**. 같은 prompt로 시드/타임스탬프 다르게 3회 시도한 흔적 — Time-lapse 톤 잡기가 가장 어려운 컷이었다는 데이터.

**채택**: YouTube `https://www.youtube.com/shorts/VKzCareMI4Q` 게시.

---

## 매핑 표 — ep_pd1_invisible_mountain (보이지 않는 산, 8개) — YouTube 게시됨

콘티 원본: **18분 콘티(`05_developed/04_pd1-5.json`, 6시퀀스)의 시퀀스 1·3·4·6 60초 압축**.

→ **GAP — 60초 별도 콘티 파일 없음**. 다른 60초 ep는 `shorts_pdX.md`로 컷 단위 콘티가 있지만, invisible_mountain은 18분 풀 콘티만 존재. 작업자가 18분 콘티에서 *시퀀스 1·3·4·6*만 60초 안에 압축하도록 *직접 머리로* 매핑한 흔적. 파일명 키워드(Aerial / Ground-level / First-person POV / Final restrained)로 시퀀스 추정 가능.

| # | 추정 컷 | 18분 콘티 시퀀스 | duration | style 키워드 | mp4 파일명 (Style 발췌) | 크기 |
|---|---|---|---|---|---|---|
| 1 | 위성 좌표 진입 (Aerial 짧은) | 시퀀스 1 콜드오픈 위성 시점 | 4s | Aerial satellite | `4 seconds_Style_ Aerial satellite.mp4` | 1.5MB |
| 2 | 위성 좌표 연속 | 시퀀스 1 후반/줌인 | 4s | Continued aerial | `4 seconds_Style_ Continued aerial.mp4` | 1.8MB |
| 3 | 위성 좌표 6초 변형 | 시퀀스 1 또는 5 위성 재현 | 6s | Aerial satellite | `6 seconds_Style_ Aerial satellite.mp4` | 2.1MB |
| 4 | 능선 1인칭 시야 (변형 1) | 시퀀스 3 행군 궤적 | 6s | Dynamic ground-level | `6 seconds_Style_ Dynamic ground-le.mp4` | 3.7MB |
| 5 | 능선 1인칭 시야 (변형 2) | 시퀀스 3 행군 궤적 (재생성) | 6s | Dynamic ground-level | `6 seconds_Style_ Dynamic ground-le_153249.mp4` | 2.4MB |
| 6 | 1인칭 POV (안개·활엽수림) | 시퀀스 4 1인칭 시야 시뮬 | 6s | First-person POV | `6 seconds_Style_ First-person POV.mp4` | 4.4MB |
| 7 | 위성 좌표 7초 (장 컷) | 시퀀스 1 또는 5 (장 컷) | 7s | Aerial satellite | `7 seconds_Style_ Aerial satellite.mp4` | 3.9MB |
| 8 | 마무리 정지 컷 | 시퀀스 6 엔딩 좌표 1,200점 | 8s | Final restrained | `8 seconds_Style_ Final restrained.mp4` | 1.7MB |

**총 8개** = 4 + 4 + 6 + 6 + 6 + 6 + 6 + 8 ≈ 46초 분량. 60초 쇼츠 8컷에 충분히 들어감. 다만 컷 순서 메타파일은 부재 — 작업자가 파일명 키워드 + 18분 콘티 시퀀스를 *직접 대조*해야 함. 

**채택**: YouTube `https://www.youtube.com/shorts/an6yJBIoBG0` 게시 — *60초 별도 콘티 없이도* 18분 콘티의 시퀀스 분리만으로 게시까지 도달한 흔적.

---

## 매핑 표 — _unsorted (5/5 초기 톤 테스트 2개)

5/5 채널 컨셉 회의 직전, *톤 결*을 잡기 위한 초기 테스트.

| 파일 | 의도 | 크기 |
|---|---|---|
| `0505_documentary_infographic.mp4` | 다큐멘터리 + 인포그래픽 톤 시도 | 3.9MB |
| `0505_intimate_historical_drama.mp4` | 친밀한 역사 드라마 톤 시도 | 2.1MB |

→ 이 두 톤이 비교되며 *친밀한 역사 드라마*는 5/4 archived_v2 폐기와 같은 결로 폐기. *다큐멘터리 인포그래픽*이 살아남아 60초 콘티 톤의 기본이 됨.

---

## 로컬 빈 폴더 — 세 종류 (sync 대기 / 시즌형 흡수)

| 폴더 | 채널 상태 | 콘티 | 로컬 mp4 부재 사유 |
|---|---|---|---|
| `ep_pd2_5_stars1438/` | **채널 게시 완료** ([1DU3Ciia_zw](https://www.youtube.com/shorts/1DU3Ciia_zw) "1438년의 별: 조선은 하늘을 어떻게 기록했나") | **콘티 GAP — `shorts_pd2.md` 부재** (v4_short 7분 콘티만 있음) | 원격 환경에서 작업 중 — mp4 파일은 곧 rsync로 가져올 예정 |
| `ep_pd3_lunch10000/` | **채널 게시 완료** ([GPUglXi4o4c](https://www.youtube.com/shorts/GPUglXi4o4c) 점심값) | `shorts_pd3.md` 9컷 ✓ | 원격 환경에서 작업 중 — mp4 파일은 곧 rsync로 가져올 예정 |
| `ep_pd4_1903photo/` | **채널 미게시** | `shorts_pd4.md` 9컷 ✓ | 콘티 작성됐으나 영상 미생성. 시즌형 진화로 흡수 — PD4 글로벌 페르소나는 60초보다 시즌 단위 다큐에 더 적합하다는 운영 시그널 |

→ stars1438·lunch10000은 *로컬에서 빈 폴더로 보일 뿐 실제로는 채널 운영 중*. 1903photo만 채널 미게시 + 시즌형 흡수로 유지.

### GAP — 콘티 부재 2건

| GAP | 운영 |
|---|---|
| **invisible_mountain 60초 콘티 부재** | 18분 콘티(`05_developed/04_pd1-5.json`) 시퀀스 1·3·4·6 분리만으로 mp4 8개 생성 → 채널 게시 도달 |
| **1438-star 60초 콘티 부재 (`shorts_pd2.md` 없음)** | 7분 콘티(`v4_short/05_pd2-5_construction.md`)에서 60초로 *건너뛰기 운영*. 로컬 mp4는 mbp2 sync 대기 / 채널은 게시 완료 |

→ *콘티 → 영상 → 채널*이라는 표준 워크플로우가 *항상 따라가지는 않았다*는 운영 데이터. 콘티 파일 없이도 채널 게시까지 도달했다는 흔적이지만, 다음 사이클에서 콘티 표준화·자동화 도구화의 시그널이기도 함.

---

## prompt → 출력 prompt 변환 흐름

콘티(예: shorts_pd1.md CUT 01)에서:

```
[Aspect ratio] 16:9 horizontal 1920x1080
[Duration] 8 seconds
[Style] Documentary archival reconstruction, 1930s Korean newspaper office, ...
[Scene] Extreme close-up of a wooden type-case drawer being slowly slid open ...
[Composition] Top-down view, hand entering from lower-right of frame, ...
[Voiceover - Korean, calm middle-aged male documentary tone] "1936년 8월 25일 밤, 동아일보 조판실."
[Sound] Soft wooden drawer slide, faint distant tram bell ...
[Negative] No visible faces, no readable Korean or Chinese text on type pieces, ...
```

→ Seedance 2.0이 mp4 파일명에 *Style* 키워드를 자동 임베드함:
`Seedance 2_0 - _Aspect ratio_ 169 horizontal 1920x1080_Duration_ 8 seconds_Style_ Documentary archiv.mp4`

→ 파일명만 봐도 콘티 컷과 매핑 가능. **mp4 → 콘티 역추적의 핵심 키**는 *Duration + Style 첫 단어 2-3개*.

---

## QC 체크 (실 출력에서)

콘티에 명시된 환각 차단 룰이 실제 출력에서 어떻게 통과했는가:

| 룰 | 통과 여부 (육안 기준) |
|---|---|
| 인물 얼굴 클로즈업 0건 | ✓ (typesetter1936 전 컷 손·실루엣·물체) |
| 한자/한글 활자 추상 디테일만 | ✓ (실제 글자 식별 불가) |
| 일장기 직접 렌더 X | ✓ (가슴 부위 *연필 동그라미*로 우회) |
| 컬러 일관성 (sepia-amber palette) | ✓ (10개 모두 같은 톤) |
| 컷당 4-8s 단일 클립 | ✓ (Sora 2 8s 한계 내 운용) |

→ 컷-레벨 디렉터 가설(메타 가설 1)의 *후처리 검수 단계 데이터*. 콘티가 깊을수록 출력의 환각 차단도 단단함.

---

## 다음 단계 (영상 운용)

이 출력물은 *프리비주얼* 단계. 실제 60초/3분 *최종 운용 영상*은:
1. 후처리 합성 (워터마크 + 자막 + 출처 캡션)
2. 음성 합성 (ElevenLabs v3 한국어 + SSML 호흡 마크)
3. 음악·SFX 합성 (Suno v5 또는 SFX 폴리)
4. 컬러 그레이딩 (DaVinci Resolve)
5. 자막 SRT (한국어 + 영문)

이 5단계가 다음 사이클의 작업. 현재 사이클은 *콘티 + 컷 단위 프리비주얼*까지.

---

## 산출물 (이 폴더)

| 항목 | 내용 |
|---|---|
| 이 README | mp4 매핑 표 + 콘티 → 출력 변환 흐름 |
| (mp4 파일은 git 미포함) | 원본 위치 명시 — `runs/cycle-001/v5_60sec/outputs/` |

→ 영상 mp4를 보고 싶으면 원본 폴더 직접 접근. 깃에는 매핑만.

---

## 다음 단계

`10_site/` — dasibonda-site 링크 (별도 세션 작업).

---

*복사: 2026-05-07 / 영상 원본 위치: runs/cycle-001/v5_60sec/outputs/ (수정 금지)*
