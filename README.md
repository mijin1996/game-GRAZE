# 🦋 GRAZE (game-GRAZE)

> **GRAZE** : "살짝 스치다"라는 뜻
> 한 줄 소개: (직접 작성)
> 예) 사방에서 날아오는 몬스터의 총알을 아슬아슬하게 피하며 오래 버티는 3D 닷지 게임

---

## 📜 개발 과정 히스토리

### Phase 1 — 기초 뼈대 (교수님 수업 · `Dodge 초기스크립트/`)
수업에서 짠 닷지 게임 초기 스크립트로 **피하기 게임의 기본 루프**를 만들었다.

| 사용한 개념 | 적용된 곳 |
|---|---|
| Rigidbody 속도 이동 + `Destroy(시간)` | 총알이 앞으로 날아가고 3초 뒤 사라짐 |
| 랜덤 주기 생성 + `LookAt` | `BulletSpawner`가 랜덤 간격으로 플레이어를 향해 발사 |
| 생존 시간 + `PlayerPrefs` | `GameManager`가 버틴 시간을 세고 최고 기록 저장 |
| 조이스틱 입력 | `PlayerInput` 이동 |
| Transform 이동·회전 연습 | `Move_n_Rotate`, `Rotator` |
| 씬 전환 | `SceneChange` (버튼용) / `SceneManager.LoadScene` (매니저용) |

### Phase 2 — 기능 확장 · 리팩토링 (ME)

**① 플레이어 조작**
- 조이스틱 + 키보드(방향키·WASD) 둘 다 지원, 조이스틱 종류 `DynamicJoystick`으로 변경
- 점프: 물리 대신 직접 만든 중력(`jumpPower`, `gravity`)으로 위아래 속도 계산
- 벽 막힘 판정: `SphereCastAll`로 앞을 검사해 건물·나무를 통과하지 않게 (낮은 턱 `stepHeight`·여유 거리 `skinWidth`는 통과)
- 소리: 걸을 때만 발소리 루프, 점프 효과음

**② 적 · 총알**
- 몬스터가 쏘는 순간 공격 애니메이션, 게임오버 시 대기 동작 + 발사 중지
- 총알이 벽·지형에 부딪히면 이펙트 후 제거 (몬스터 자신은 무시)
- 맵 회전, 적 추가

**③ 게임 흐름 · UI**
- 게임오버 시 시간 글자·점프 버튼 숨김, 클릭(R키)으로 재시작
- 시작(Intro) 화면

**④ 에디터 자동화 (`Assets/Scrips/Editor/`)**
- `GrazeIntroSetup`: Intro 씬(배경·제목·START 버튼) 자동 생성
- `GrazeMapColliders`: 움직이지 않는 오브젝트의 콜라이더를 Mesh Collider로 일괄 변환
- `GrazeSoundSetup`: 플레이어 AudioSource 자동 연결

#### 💭 고민한 점 · 배운 점
- (직접 작성)
- (직접 작성)

---

## 🛠 기술 스택
- **Language:** C#
- **Engine:** Unity 6 (6000.5.3f1)
- **그 외:** Joystick Pack, Cartoon FX Remaster

---

## 📁 문서
- [`docs/Proposal/common_Index.md`](docs/Proposal/common_Index.md) — 기획서 (컨셉 ~ 사업화 · 법무) · [needFix](docs/Proposal/common_needFix.md)
- [`docs/MeMemo.md`](docs/MeMemo.md) — 처음 작성한 README 메모
