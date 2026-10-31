# 출처·수정 범위

원본 전체를 무검증 설치하는 패키지가 아니다. 아래 고정 버전에서 지침을 선별하고 제공 환경에 맞게 좁힌 수정본이다. 원저작자의 공식 배포나 보증을 의미하지 않는다.

## 현재 구성과 수정

work-session 지침과 PLAN·DECISIONS 템플릿은 독자 작성했다. 요구·질문/실제 답변·계획·진행/검증 근거를 PLAN으로 통합하고, 중요한 판단만 DECISIONS에 보존한다. 필요한 보조 지침만 단계에 맞춰 읽는다. 사용자 보고와 작업 문서는 한국어로 작성한다. 실행 엔진·훅·전역 설정은 포함하지 않는다.

보조 Skills는 아래 원본의 수정판이며 원저작자의 공식 배포·보증을 의미하지 않는다. 다음 표는 원저작 출처와 수정 방향을 요약하고, manifest의 changes는 현재 수정 내역, files는 현재 배포 파일의 SHA-256을 기록한다. 각 폴더의 원본 라이선스를 유지한다.

1.1.0에서는 실제 과제와 위험에 따른 경로 선택, 조건부 읽기 전용 독립 리뷰, 도구 부재·오류 시 순차 검토/직접 검증, 실제 중단 시 PLAN 안의 상태 스냅샷과 재개 검증을 독자 작성하여 추가했다. 필수 새 도구·추가 Skill·전역 설정은 없다. 세부 변경은 CHANGELOG.md에 기록한다.

| Skill | 원본 | 커밋 | 라이선스 | 수정 |
|---|---|---|---|---|
| grill-me | [mattpocock/skills](https://github.com/mattpocock/skills/blob/59db609eb1e18aaf59b63284d0e52255aff0c63c/skills/productivity/grill-me/SKILL.md) | `59db609eb1e18aaf59b63284d0e52255aff0c63c` | MIT | Replaced host-specific wrapper with a relative read of sibling grilling; removed Claude-only frontmatter; retained explicit invocation policy from existing Codex metadata. |
| grilling | [mattpocock/skills](https://github.com/mattpocock/skills/blob/59db609eb1e18aaf59b63284d0e52255aff0c63c/skills/productivity/grilling/SKILL.md) | `59db609eb1e18aaf59b63284d0e52255aff0c63c` | MIT | Limit interview to material task decisions; inspect local facts first; make delegation conditional on available permitted tools; continue authorized work after decisions are answered. |
| verification-before-completion | [obra/superpowers](https://github.com/obra/superpowers/blob/2ce8aa15d05bd57213e6f746f953aafb7ded7a8b/skills/verification-before-completion/SKILL.md) | `2ce8aa15d05bd57213e6f746f953aafb7ded7a8b` | MIT | Add task-scoped validation guidance; no zero-test/fully-skipped success; no new tooling merely to satisfy a generic checklist. |
| frontend-design | [anthropics/skills](https://github.com/anthropics/skills/blob/dbd4588f9e1033efb41dad4bef2f7947c8993d44/skills/frontend-design/SKILL.md) | `dbd4588f9e1033efb41dad4bef2f7947c8993d44` | Apache-2.0 | Retain design guidance; replace automated screenshot review with participant manual preview; prioritize actual task workflow over visual expansion. |
| diagnosing-bugs | [mattpocock/skills](https://github.com/mattpocock/skills/blob/59db609eb1e18aaf59b63284d0e52255aff0c63c/skills/engineering/diagnosing-bugs/SKILL.md) | `59db609eb1e18aaf59b63284d0e52255aff0c63c` | MIT | Replace headless-browser/HITL script requirements with local CLI/HTTP tests and participant manual preview; restrict load and external operations. |
| api-tester | [RightNow-AI/openfang](https://github.com/RightNow-AI/openfang/blob/acf2587e46be174c10200489c9a2d23a39a98aeb/crates/openfang-skills/bundled/api-tester/SKILL.md) | `acf2587e46be174c10200489c9a2d23a39a98aeb` | MIT/Apache-2.0 | Restrict to task-authorized business API; remove rapid rate-limit probing, secret-bearing verbose traces and alternate-network advice; no external model API. |
| api-and-interface-design | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills/blob/aeac41d4d005999432bb7312f7ff06383a91d59d/skills/api-and-interface-design/SKILL.md) | `aeac41d4d005999432bb7312f7ff06383a91d59d` | MIT | Adapt contract-first API/interface guidance to task-sized CRUD, validation, storage and frontend integration; make pagination, idempotency infrastructure and versioning conditional; use local CLI/HTTP checks and participant manual preview; no external AI or global configuration. |

각 배포 파일의 SHA-256은 manifest.json에 있다. 원본 커밋과 현재 수정 파일의 해시는 구분한다. 상세 수정 내용은 manifest의 changes에 기록한다.

1.2.0에서는 역할별 책임과 기존 지침을 보존하는 AGENTS 포인터, 15개 단계·11개 유형별 요청 가이드, 선택형 작업 지도·검증 상태, 실제 전환 시 쓰는 HANDOFF 양식을 추가했다. 가이드·양식은 현재 사용자 요구를 바탕으로 범용 문구로 정리했으며, 비공개 조사 문서와 행사 고유 정보를 배포하지 않는다. 기존 보조 7종의 본문·원저작 고지는 유지한다.

1.2.1에서는 프롬프트 참고서 26개를 루트 PROMPTS.md의 사용자 전용 문서로 분리하고 에이전트의 자동 읽기·양식 추천 경로를 제거했다. grilling은 중요한 결정 질문으로 범위를 좁히고 승인된 일반 구현은 계속하도록 보완했다. API·단계 진행 예시, 기존 AGENTS의 명시적 재독·비충돌 갱신과 옛 가이드의 안전한 이전 안내를 정리했다.
