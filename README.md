# Physical AI 연구개발·GitHub 공유 파트너

**AI와 한국어로 연구개발을 의논하고 실행하며, 결과물을 팀원이 내려받아 활용할 수 있게 공유하기 위한 Codex 스킬 모음입니다.**

문제의 원인을 정확히 모르거나 Git 명령을 잘 몰라도 현재 상황과 원하는 결과로 시작할 수 있습니다. AI가 접근 가능한 코드·문서·로그를 읽고 필요한 작업과 확인을 수행하도록 구성했습니다.

## 어떤 스킬을 선택하나요?

| 스킬 | 이런 요청에 사용합니다 | 상세 안내 |
|---|---|---|
| `physical-ai-rnd-partner-ko` | 연구 방향·대안 의논, 설계·구현·디버깅, 실험·평가·통합·유지보수 | [연구개발 파트너 안내](docs/physical-ai-rnd-partner-ko.md) |
| `github-rnd-sharing-ko` | README 작성, GitHub 게시, 팀원의 첫 실행, 모델·데이터 전달, branch·PR·리뷰·갱신 | [공유 파트너 지침](skills/github-rnd-sharing-ko/SKILL.md) |

두 스킬은 독립적으로 설치할 수 있습니다. 논문·개념 학습용 `physical-ai-mentor-ko`는 별도 스킬이며 이 저장소에 포함하지 않았습니다.

## 빠른 시작

### 1. 필요한 스킬 설치

Codex에서 다음 메시지를 입력하세요. 아래는 GitHub 공유 파트너를 설치하는 예시입니다.

```text
$skill-installer
https://github.com/eunsu0325/Physical-AI_R-D_Partner_skill/tree/main/skills/github-rnd-sharing-ko
이 경로의 스킬을 설치해줘.
```

연구개발 파트너가 필요하면 다음 경로를 사용합니다.

```text
$skill-installer
https://github.com/eunsu0325/Physical-AI_R-D_Partner_skill/tree/main/skills/physical-ai-rnd-partner-ko
이 경로의 스킬을 설치해줘.
```

두 개를 모두 쓰려면 두 경로를 함께 알려주고 설치를 요청해도 됩니다. 설치 후 다음 메시지에서 사용하세요. 목록에 보이지 않으면 설치 위치·중첩 폴더·비활성화 여부를 확인하고 Codex를 다시 시작하세요.

### 2. 현재 상황으로 요청

```text
$github-rnd-sharing-ko
이 연구 코드를 팀원이 내려받아 실행할 수 있게 정리해줘.
실제 코드와 실행 방법을 확인해서 README와 필요한 안내를 작성하고,
가능한 최소 실행까지 확인해줘. 오늘은 GitHub 게시 전 준비까지만 해줘.
```

```text
$physical-ai-rnd-partner-ko
상자를 놓치는데 원인을 모르겠어. 그립 문제 같지만 확신은 없어.
현재 코드와 로그를 보고 내 추측도 검토하면서 필요한 조사와 수정을 진행해줘.
```

완성된 요구사항이나 정해진 프롬프트 양식은 필요하지 않습니다. 접근할 저장소·자료와 현재 목표, 실행 가능한 환경을 알려주면 도움이 됩니다.

## GitHub 공유 파트너가 하는 일

`github-rnd-sharing-ko`는 공유 목적에 맞춰 다음 작업을 선택합니다.

| 상황 | 수행 방향 |
|---|---|
| 로컬 연구를 처음 올림 | 실제 Git 루트·원격·이력·변경 확인, 공유 파일 선별, README·자산 안내 준비, 요청된 게시 |
| 팀원이 처음 실행함 | 정확한 코드·자산 취득 경로, 환경 구성, 최소 명령과 정상 결과 연결 |
| README가 오래됐음 | 실제 entrypoint·인자·설정·검증 기록과 문서를 대조하고 갱신 |
| 변경을 함께 검토함 | 기존 CONTRIBUTING·AGENTS·PR 템플릿을 읽고 branch/fork·PR·리뷰 흐름에 맞춰 공유 |
| 이미 받은 코드를 갱신함 | 미커밋 작업과 tracking 상태를 확인하고 원격 조회·통합을 구분 |
| 모델·데이터·mesh가 큼 | 일반 Git/LFS/Release/외부 저장소의 적합성, 버전·해시·접근·배치 조건 정리 |

게시를 요청하면 준비한 자료와 가능한 검증을 마친 뒤 승인된 대상에 반영하고 원격 내용을 확인합니다. 기존 작업을 보존하며, 준비 요청을 공개 게시·설정 변경으로 확대하지 않습니다. 같은 저장소에서의 협업과 fork 기여, 최초 clone과 이후 갱신은 상황에 따라 구분합니다.

### README 작성 기준

팀원이 다음을 판단할 수 있도록 씁니다.

1. 개발 목적과 현재 사용할 수 있는 기능.
2. 실제 검증한 환경·기준 버전·중요한 제한.
3. 코드와 필요한 모델·데이터의 취득 및 배치 방법.
4. 처음 수행할 한 가지 작은 실행과 필요한 선행 조건.
5. 실제 확인한 정상 출력·생성 파일·값과 확인 방법.
6. 상세 사용·기여·도움·출처로 이어지는 경로.

실제 코드에 없는 명령·자산 URL·성능을 만들지 않습니다. 공식 지원 조건과 시험한 환경, 설명용 의사코드와 실행 가능한 예제를 구분합니다. 저장소의 목적과 규모에 맞춰 문서를 나누며 모든 프로젝트에 동일한 목차나 문서 묶음을 강제하지 않습니다. [README 작성 지침](skills/github-rnd-sharing-ko/references/readme-writing.md)

### 사용 예시

```text
$github-rnd-sharing-ko
README에 있는 명령이 실제 코드와 맞는지 확인해서 수정해줘.
팀원이 회사 GPU 서버에서 실행하고 결과를 로컬로 가져오는 경로를 설명해줘.
현재 실행할 수 없는 항목은 미확인으로 남겨줘.
```

```text
$github-rnd-sharing-ko
지정한 기존 GitHub 저장소에 이 변경을 올리고 PR을 만들어줘.
저장소의 기여 규칙과 PR 양식을 먼저 확인하고,
문제·달라진 행동·실제 검증·남은 조건을 최종 변경에 맞춰 작성해줘.
```

## 설치·업데이트 상세

이 저장소는 텍스트 지침과 참고문서입니다. 스킬 설치 자체에는 GPU·ROS·시뮬레이터·모델 가중치가 필요하지 않습니다. 실제 연구 코드 실행에는 해당 프로젝트의 환경과 접근 권한이 필요합니다.

권장 경로는 위의 Codex Skill Installer 요청입니다. 수동 설치 시에는 다음처럼 **스킬 폴더 전체**를 복사합니다. 아래는 Git과 POSIX 호환 셸을 사용하는 macOS/Linux 예시입니다.

```bash
git clone https://github.com/eunsu0325/Physical-AI_R-D_Partner_skill.git
cd Physical-AI_R-D_Partner_skill

mkdir -p "$HOME/.agents/skills"
if [ -e "$HOME/.agents/skills/github-rnd-sharing-ko" ]; then
  echo "이미 설치된 사본이 있습니다. 위치와 로컬 수정을 확인한 뒤 업데이트하세요."
else
  cp -R skills/github-rnd-sharing-ko "$HOME/.agents/skills/"
fi
```

연구개발 파트너는 위 예시의 폴더 이름을 `physical-ai-rnd-partner-ko`로 바꿉니다. 최종 위치에서 `<스킬 이름>/SKILL.md`, `agents/`, `references/`가 바로 보여야 합니다. `SKILL.md`만 복사하면 참고문서가 빠집니다.

개인 수동 설치의 `~/.agents/skills` 예시와 내장 설치기가 사용하는 환경별 위치는 다를 수 있습니다. 현재 사본이 `~/.codex/skills` 등에 있다면 그 위치부터 확인하고 중복 사본을 만들지 마세요. 특정 프로젝트에서만 쓰려면 해당 프로젝트의 `.agents/skills/<스킬 이름>/` 아래에 폴더 전체를 둘 수 있습니다. [Codex 공식 스킬 문서](https://learn.chatgpt.com/docs/build-skills)

Windows에서는 같은 폴더 구조로 사용자 홈 또는 프로젝트의 스킬 위치에 복사하세요. 위 POSIX 셸 명령을 PowerShell에서 그대로 실행하는 방식은 확인하지 않았습니다.

이미 clone한 저장소의 업데이트는 그 checkout에서 상태와 추적 branch를 먼저 확인합니다. 미커밋 변경이 없고 현재 branch가 대응 원격보다 뒤처지기만 했다면 다음이 가능한 경로입니다.

```bash
git pull --ff-only
```

분기·충돌·로컬 수정이 있으면 상태에 맞게 처리하세요. 소스 저장소를 갱신해도 별도로 복사한 설치 사본이 자동 갱신되지는 않습니다. 설치 위치와 개인 수정을 확인한 뒤 해당 스킬 전체의 업데이트를 요청하세요.

## 저장소 구성

```text
Physical-AI_R-D_Partner_skill/
├── README.md
├── docs/
│   └── physical-ai-rnd-partner-ko.md
└── skills/
    ├── physical-ai-rnd-partner-ko/
    │   ├── SKILL.md
    │   ├── agents/openai.yaml
    │   └── references/
    └── github-rnd-sharing-ko/
        ├── SKILL.md
        ├── agents/openai.yaml
        └── references/
            ├── readme-writing.md
            ├── publishing-and-assets.md
            ├── clone-and-verification.md
            ├── team-collaboration.md
            └── sources-and-adoption.md
```

GitHub 공유 파트너의 참고문서:

- [README 작성](skills/github-rnd-sharing-ko/references/readme-writing.md): 독자별 흐름, 실제 명령·정상 출력, 문서 역할과 링크.
- [게시·자산](skills/github-rnd-sharing-ko/references/publishing-and-assets.md): Git 이력, 공유 파일, 모델·데이터·라이선스.
- [clone·검증](skills/github-rnd-sharing-ko/references/clone-and-verification.md): submodule/LFS/권한, 실행 환경과 근거의 범위.
- [팀 협업](skills/github-rnd-sharing-ko/references/team-collaboration.md): branch/fork, issue·PR·리뷰, 동기화와 충돌.
- [출처·채택 판단](skills/github-rnd-sharing-ko/references/sources-and-adoption.md): 공식 문서, 공개 스킬, LeRobot·mjlab 사례와 적용 판단.

본문에는 공통 판단 기준을 두고 상세 자료는 현재 작업에 필요한 것만 읽도록 구성했습니다. 실행을 위한 외부 스킬의 자동 설치나 필수 의존성은 추가하지 않았습니다.

## 근거와 검증 범위

GitHub 공유 파트너는 Git/GitHub 공식 문서, Google의 변경 검토 지침, 문서 작성 방법, 실제 LeRobot·mjlab의 문서와 PR을 참고했습니다. GitHub가 소개하는 커뮤니티 스킬 5개와 템플릿 21개, OpenAI의 GitHub 작업용 스킬 3개도 검토하고 수용·수정·제외 이유를 기록했습니다. 원문 스킬이나 템플릿을 이 패키지에 복제하지 않았습니다.

GitHub Skills 교육 과정, GitHub가 소개하는 community-created Agent Skills 모음, OpenAI가 제공하는 GitHub 작업용 Codex 스킬은 작성 주체와 용도가 다릅니다. 이 저장소의 두 스킬은 개인적으로 작성한 지침이며 GitHub·OpenAI의 공식 제품이나 인증 스킬을 뜻하지 않습니다.

공유 스킬 작성 과정에서는 형식·내부 참조를 검사하고 임시 코드에 대한 README 작성·예제 실행, 서로 다른 저장소별 PR 관례 두 가지의 적용 결과를 확인했습니다. 스킬 없는 비교 사례도 기본 작업을 수행했으므로 이 결과로 생산성 향상이나 실패 교정 효과를 주장하지 않습니다. 실제 연구 프로젝트의 GPU·SIM·실물 성능 검증은 별도입니다. 연구개발 파트너의 근거와 검증 범위는 [상세 안내](docs/physical-ai-rnd-partner-ko.md#연구-근거와-검증-범위)를 참고하세요.

## 기여와 유지관리

변경은 실제 누락이나 사용 사례를 근거로 작게 제안해 주세요. 관련 지침·링크·메타데이터를 함께 확인하고, 어떤 행동을 시험했고 무엇을 실행하지 않았는지 설명하면 검토에 도움이 됩니다. 스킬 파일만 바뀌면 GPU 학습이나 실물 테스트를 요구할 이유는 없습니다.

스킬의 지원 범위가 달라지면 이 README와 관련 문서를 함께 갱신합니다. 비공개 프로젝트 코드·로그·자격증명·회사 장비 정보를 공통 지침에 넣지 마세요. 아직 지정되지 않은 라이선스나 운영 약속을 임의로 추가하지 않습니다.

## 라이선스

현재 이 저장소에는 별도의 `LICENSE` 파일이 지정되어 있지 않습니다. 인용된 연구·외부 문서·스킬의 권리는 각 원저작자에게 있으며, 링크된 자료의 라이선스가 이 저장소나 연구 자산에 자동 적용되는 것은 아닙니다.
