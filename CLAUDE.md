# rutter — AI 에이전트 지침

이 저장소는 Followingseas 조직의 공용 지침서다. AI 에이전트는 다음을 따른다.

## 저장소 관리

- rutter의 git은 지침 문서와 메타 파일만 관리한다 (`.gitignore`, `README.md`, `rutter.yaml`, `CLAUDE.md`, `defaults.yaml`, `docs/`, `policies/`)
- `.gitignore`는 전체 무시(`/*`) 후 관리 대상만 선택적으로 허용하는 구조다. **사용자가 명시적으로 요청하지 않는 한 절대 수정하지 않는다**
- 조직 프로젝트는 이 저장소 밑에 클론하지 않는다 — 각 프로젝트는 임의 위치에서 [Pilot](https://github.com/followingseas/pilot)으로 이 지침서를 연결받는다 (`pilot connect` / `pilot init`)

## 이 저장소에서 작업할 때

- 문서는 사람과 AI가 함께 읽는다. 사람이 읽기 좋게 쓰되, 에이전트가 그대로 실행할 수 있을 만큼 구체적으로 쓴다
- 모든 규약 문서에는 **왜(Why)** 를 함께 적는다
- 조직 구조가 바뀌면 `docs/maps/`의 지도를 먼저 갱신한다
- 기계 검증 가능한 규칙은 `policies/`의 PolicySet YAML(rule id·level·statement·rationale·checks)에도 등록한다 — 문서는 설명, PolicySet은 검증 담당

## Git 워크플로우

- GitHub Flow: `main` 단일 브랜치, 작업은 `feature/<이름>` 브랜치 → PR → main 머지
- 커밋 메시지·PR·문서는 한글로 작성한다 (코드 식별자는 영어)

## 다른 저장소와의 관계

- 조직 각 저장소의 `CLAUDE.md`가 이 저장소의 규약을 참조한다
- 규약이 충돌하면 **개별 저장소의 지침이 우선**한다 (rutter는 기본값)
