# Rutter

> The shared sailing directions of Followingseas — read by humans and AI alike.

해도(海圖)가 귀하던 시절, 항해사들은 선배들이 물길·위험·입항법을 손으로 적어 물려준 **항로 지침서(rutter)** 에 의지해 바다를 건넜습니다. Rutter는 Followingseas 조직의 그 지침서입니다 — **사람과 AI 에이전트가 함께 펼쳐 보는** 규약과 지도를 담습니다.

## 이 저장소가 담는 것

| 구역 | 내용 |
|------|------|
| `conventions/` | 항로 규칙 — 커밋 메시지, 브랜치 전략(GitHub Flow), 코드 리뷰, 커뮤니케이션 언어 등 조직 공통 규약 |
| `charts/` | 연안 지도 — 프로젝트 맵, 저장소 인덱스, 아키텍처 개요 등 조직을 조망하는 문서 |
| `CLAUDE.md` | AI 승무원의 진입점 — AI 에이전트가 조직 저장소에서 작업할 때 따라야 할 지침의 시작점 |

## 원칙

- **사람과 AI가 같은 지침서를 본다** — 문서는 사람이 읽기 좋게 쓰되, AI 에이전트가 그대로 따를 수 있을 만큼 구체적으로 쓴다
- **규칙에는 이유를 남긴다** — 왜(Why) 없는 규칙은 지켜지지 않는다. 각 규약에는 배경을 함께 적는다
- **지도는 현행을 반영한다** — `charts/`는 조직의 현재 상태를 그린다. 낡은 지도는 좌초를 부르므로, 구조가 바뀌면 지도부터 고친다

## 사용법

- **사람**: 조직에서 작업을 시작하기 전 `conventions/`를 읽고, 길을 잃으면 `charts/`를 펴세요
- **AI 에이전트**: 각 저장소의 `CLAUDE.md`가 이 저장소의 해당 문서를 참조합니다. 규약 충돌 시 개별 저장소의 지침이 우선합니다

## 상태

초기 구축 중입니다. 규약과 지도가 채워지는 대로 이 README의 목차가 갱신됩니다.

- `rutter.yaml` — Pilot이 읽는 manifest
- `charts/projects.md` — 조직 저장소 조망 지도

## Pilot으로 사용하기

이 저장소는 [Pilot](https://github.com/followingseas/pilot)이 읽는 **레퍼런스 rutter 인스턴스**입니다. 프로젝트가 어디에 클론돼 있든 이 지침서를 AI 에이전트에 연결할 수 있습니다.

```bash
pilot connect https://github.com/followingseas/rutter --id followingseas
cd <어느 프로젝트든>
pilot context          # 적용 규약 확인
pilot init             # 프로젝트에 선언 파일·스텁 생성
```

자기 조직의 rutter를 만들려면 이 저장소의 구조와 `rutter.yaml`을 본보기로 삼으면 됩니다.

---

<sub>Part of <a href="https://github.com/followingseas">Followingseas</a></sub>
