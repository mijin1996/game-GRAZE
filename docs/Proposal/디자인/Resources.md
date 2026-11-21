# 리소스 (아트 · 사운드) 명세 — GRAZE

> 문서 세트: [목차](../Index.md) · 기획: [컨셉](../기획/Concept.md) · [시스템](../기획/System.md) · [전투·개체](../기획/Combat_Entity.md) · [레벨 디자인](../기획/LevelDesign.md) · [밸런스](../기획/Balance.md) · 사업·운영: [사업 검토](../대표/Business.md) · [요구사항·로드맵](../기획/Requirements.md) · [Business Model](../기획/Monetization.md) · [서버·데이터](../개발/Server_Data.md) · **리소스** · [로그·지표](../기획/Analytics.md) · [QA·출시](../QA/QA_Release.md) · [라이브 운영](../운영/LiveOps.md) · [사업화·법무](../대표/Business_Legal.md) · [needFix](../needFix.md)

> **문서 정보** · 문서 번호 `D09-RES` · 버전 v1.0 · 상태 `Draft` · 담당 아티스트 · 사운드 디자이너 · 최종 수정 2026-11-21 · 관련 문서 [전투·개체](../기획/Combat_Entity.md) · [사업화·법무](../대표/Business_Legal.md)

**변경 이력**

| 버전 | 날짜 | 변경 내용 | 사유 | 결정자 | 영향 범위 |
|---|---|---|---|---|---|
| v1.0 | 2026-11-21 | 최초 작성 | — | 아티스트 | — |

---

## 1. 목적
게임에 들어가는 **모든 그림 · 모델 · 소리 · 폰트의 목록 · 라이선스**를 관리해요.
> **규칙:** 라이선스가 `확인됨`이 아닌 리소스가 있으면 출시하지 않아요.

## 2. ⚠️ 먼저 고칠 것 — 상업 출시 불가 리소스
| 리소스 | 위치 | 문제 | 대응 |
|---|---|---|---|
| **Glue Gun 폰트** (`Glue Gun.otf`) | `Fonts/` · `Balls/[UIFabrica]TrollNest_Free_v01/05.FONT/` | 동봉 라이선스가 **`FSLA_NonCommercial_License`** (비상업 전용) — 광고 · 결제가 있는 게임은 상업 이용 | 상업 라이선스 구매(동봉 "Get Commercial License" 링크) 또는 OFL 폰트로 교체 |
| **arial.ttf** | `Ultimate 10 Plus Shaders/` | Arial은 Microsoft 소유 폰트 — 게임에 넣어 배포하면 안 될 수 있음 | 셰이더 데모용이면 삭제, 쓰면 교체 |
| `GSHYEJAROUN-Bold.otf` | `Fonts/` | 라이선스 파일 없음 | 출처 · 상업 이용 가능 여부 확인 |
| `KakaoTalk_20261026_*.png` | `Images/` | 메신저로 받은 이미지 — 누가 만들었는지 기록 없음 | 제작자 · 사용 허락 기록 |

→ [F-03](../needFix.md#8-정할-것)

## 3. 지금 쓰는 리소스

**모델 · 그림**
| 리소스 ID | 폴더 | 쓰는 곳 | 출처 | 라이선스 |
|---|---|---|---|---|
| `MDL_PLAYER` | `RPG Tiny Hero Duo` | 플레이어 | 에셋 팩 (Asset Store 이름 기준) | ⚠️ 다운로드 기록 확인 |
| `MDL_MONSTER` | `Monster` | 몬스터 4마리 | 미확인 | ⚠️ |
| `MDL_MAP` | `Mapss` | 맵 · 건물 | 미확인 | ⚠️ |
| `MDL_BUTTERFLY` | `Butterfly (Animated)` | 배경 장식 | 에셋 팩 | ⚠️ |
| `UI_TROLLNEST` | `Balls/[UIFabrica]TrollNest_Free_v01` | UI | UIFabrica 무료 팩 | ⚠️ 팩 라이선스 확인 (폰트는 비상업) |
| `UI_JOYSTICK` | `Joystick Pack` · `Images/Joystick*` | 조이스틱 | Joystick Pack (Asset Store) | ⚠️ |
| `UI_TITLE` | `Images/GRAZE_Title.png` · `GRAZE_title_cute_noslime.png` · `Character_1920x1080.png` | 타이틀 · 인트로 | 직접 제작 추정 | ⚠️ 제작 방법(직접 · AI 생성 등) 기록 |
| `FX_CFXR_*` | `JMO Assets/Cartoon FX Remaster` | 이펙트 | Unity Asset Store (JMO) | ⚠️ 다운로드 기록 (Kino Bloom 라이선스 동봉) |
| `SHD_ULTIMATE` | `Ultimate 10 Plus Shaders` | 셰이더 | 에셋 팩 | ⚠️ (arial 포함 → §2) |

**사운드**
| 리소스 ID | 파일 · 폴더 | 쓰는 곳 | 출처 | 라이선스 |
|---|---|---|---|---|
| `BGM_*` | `25 Rpg Game Tracks/` (29곡) | 배경음 | 에셋 팩 | ⚠️ 쓰는 곡만 남기고 라이선스 저장 |
| `BGM_INTRO` | `Clips/armonicamente-game-setting-fantasy-142092.mp3` | 인트로 | 무료 음원 사이트 (Pixabay 이름 형식) | ⚠️ |
| `SFX_RPG_*` | `Clips/RPG_Essentials_Free/` | 효과음 | RPG Essentials Free 팩 | ⚠️ |
| `SFX_STEP_*` · `SFX_JUMP` · `SFX_LAND` · `SFX_DIE` | `Sounds/` · `Sounds/Player/` | 발소리 · 점프 · 사망 | 미확인 | ⚠️ |

> 같은 소리가 `Clips/`와 `Sounds/`에 두 벌 있어요 (Footstep · Jump · PlayerDie). 정리 → [F-07](../needFix.md)

## 4. 새로 필요한 리소스
| 리소스 ID | 종류 | 관련 | 상태 |
|---|---|---|---|
| `FX_GRAZE` | 스칠 때 이펙트 · 효과음 (짧고 가볍게, 0.2초) | [S-18](../needFix.md) | 대기 |
| `FX_FIRE_WARN` | 발사 예고 (몬스터 빛남 · 원) | [S-10](../needFix.md) | 대기 |
| `UI_EDGE_ARROW` | 화면 밖 몬스터 방향 화살표 | [S-19](../needFix.md) | 대기 |
| `UI_RESULT` | 결과 화면 (이번 · 최고 · 다음 목표) | [S-20](../needFix.md) | 대기 |
| `FONT_MAIN_NEW` | Glue Gun 대체 폰트 (상업 가능 · 한글 포함) | §2 | 대기 |
| `STORE_*` | 스토어 아이콘 · 스크린샷 | [QA](../QA/QA_Release.md) | 대기 |
