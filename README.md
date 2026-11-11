# photoreal-image-prompt

실제 카메라로 찍은 사진처럼 보이는 이미지를 만들기 위한 **프롬프트 작성 스킬**입니다 (Claude Code용).
장면을 한 번에 다 적을 필요 없이, Claude가 묻는 객관식 질문에 답하다 보면 프롬프트가 단계별로 완성됩니다. 결과는 **영문 프롬프트와 한국어 번역**으로 나옵니다.

> 이 스킬은 이미지를 직접 만들지 않습니다. 만들어진 영문 프롬프트를 GPT Image(ChatGPT), Gemini/Imagen, Midjourney, Flux 같은 이미지 생성 도구에 붙여넣어 사용하세요.

## 빠른 시작

1. 이 폴더(`image-skill`)에서 Claude Code를 엽니다.
2. 만들고 싶은 장면을 평소 말투로 요청합니다.

   ```
   비 오는 저녁, 재래시장에서 채소 파는 상인 사진 만들어줘
   ```

   스킬 이름을 직접 불러도 됩니다.

   ```
   /photoreal-image-prompt 눈 내리는 새벽, 편의점 앞에서 쉬고 있는 배달 라이더
   ```

3. 단계마다 나오는 질문에 답합니다. 각 선택지에는 고르면 결과가 어떻게 달라지는지 설명이 붙어 있고, 가장 사실적인 선택지에는 `(Recommended)` 표시가 있습니다. 원하는 답이 없으면 "Other"에 직접 적으면 됩니다.
4. 마지막에 나온 **English** 프롬프트를 복사해 이미지 생성 도구에 붙여넣습니다.

## 진행 순서

장면을 아래 다섯 칸으로 나눠 차례로 채웁니다.

| 단계 | 채우는 칸 | 묻는 내용 예시 | 누적 프롬프트 예시 |
|---|---|---|---|
| 1 | 피사체 | 누구인지, 나이·성별, 옷차림 상태 | a factory worker |
| 2 | + 환경 | 장소, 시간·날씨, 배경 소품 | …at an inspection line inside a manufacturing plant |
| 3 | + 동작과 끝점 | 무엇을 하다 어디서 멈추는지, 시선 | …leans over the line and stops with one hand resting on the rail |
| 4 | + 카메라 | 샷 크기, 렌즈, 심도, 앵글 | Medium shot, static camera, 50mm lens. … |
| 5 | + 조명과 스타일 | 광원·방향, 사진 장르, 색감, 사실감 디테일 | …Soft morning light from tall windows on the left. Photorealistic documentary photography. |

- 단계가 끝날 때마다 지금까지 쌓인 영문 프롬프트를 보여 줍니다.
- 요청에 이미 들어 있는 내용(예: "비 오는 저녁")은 다시 묻지 않습니다.
- 요청에 장소·시간·날씨가 이미 있으면 2단계와 3단계를 한 번에 물어서 질문 횟수를 줄입니다.
- 사람이 피사체이면 나이와 성별을 둘 다 확인합니다. 성별이 상관없다고 답하면 프롬프트에서 his/her 대신 `the rider`처럼 씁니다.

## 충돌 점검

5단계가 끝나면, 최종 프롬프트를 내기 전에 단계별 선택끼리 부딪히지 않는지 확인합니다. 예를 들어 1단계에서 어두운 데님 재킷을 고르고 5단계에서 해 질 녘 빛을 고르면, 3단계의 "젖은 어깨"는 실제 사진에서도 거의 보이지 않습니다. 이런 충돌을 찾으면 Claude가 임의로 고치지 않고 다음 중 하나를 고르도록 묻습니다.

- 앞 단계 선택을 바꾸기 (예: 재킷을 밝은 회색으로)
- 그 디테일을 빼기
- 그대로 두기 (디테일이 약하게 나올 수 있음)

충돌이 없으면 묻지 않고 넘어갑니다.

## 결과물

마지막에 다음 내용이 나옵니다.

- **최종 프롬프트 (English)**: 이미지 생성 도구에 붙여넣을 문장
- **최종 프롬프트 (한국어)**: 영문과 같은 뜻의 번역 (내용 확인용)
- **단계별 누적**: 각 단계에서 무엇이 더해졌는지
- **피해야 할 요소**: 네거티브 프롬프트를 지원하는 도구(Stable Diffusion 등, Midjourney는 `--no`)에 넣을 목록
- **사실감 체크**: 사실감을 위해 내린 선택과 그 이유

이어서 **이대로 확정 / 특정 단계 수정 / 변형 2~3개 생성** 중 하나를 고를 수 있습니다.

특정 모델을 말하면(예: "Midjourney용으로") 그 모델에 맞춘 변형본도 함께 받을 수 있습니다.

## 예시 결과

### 예시 1 — 배달 라이더

요청: `눈 내리는 새벽, 편의점 앞에서 쉬고 있는 배달 라이더 사진 만들어줘`

```
Medium wide shot, eye-level handheld camera from across the sidewalk, 35mm lens at f/2.
A Korean delivery rider, a man in his 40s in a worn padded winter jacket, sits at a plastic
table under a convenience store awning at dawn while snow falls. His scooter is parked at the
curb with a leg blanket clipped to it, and the pavement is covered in slushy snow with tire
tracks. He peels back the lid of a cup noodle and stops with steam rising into his face, eyes
down on his hands. Cool white fluorescent light spills from the store window behind him,
rimming his shoulders and the rising steam, and snowflakes are caught in the backlight.
Photorealistic documentary photography, cool desaturated palette.
```

### 예시 2 — 문래동 창작촌 커플 (리서치 포함)

요청: `비오는날 서울 문래동 창작촌 골목을 우산을 같이 쓰고 걷고 있는 남녀 커플 이미지를 만들어줘.`

실제 장소라서 Claude가 먼저 문래동 골목의 특징(철공소, 철재 더미, 낮은 시멘트 건물)을 조사하고, 불확실성 지도를 붙인 뒤 질문을 시작했습니다. 간판 글자 대신 철공소 흔적으로 장소를 드러냈습니다.

```
Full shot from behind at a three-quarter angle, eye-level handheld camera, 35mm lens at f/2.8.
A Korean couple in their late 20s walks through a narrow alley in the Mullae-dong art village
in Seoul on a rainy early evening, just after dusk. He wears a dark trucker jacket and sneakers,
and she wears a light knit sweater and a long skirt. They share a clear plastic
convenience-store umbrella. He tilts the umbrella toward her and stops mid-stride, his outer
shoulder darkened by the rain. She is mid-sentence, her face turned up toward him in profile,
while he looks ahead and listens. Stacks of rusty steel bars and pipes sit outside a small
steel workshop along the low cement buildings, and the concrete pavement is wet. Dim overcast
blue dusk light fills the alley, and warm light spills from one workshop doorway ahead,
catching the raindrops beaded on the clear umbrella. Candid street photography, muted colors
with a soft cool-warm contrast.
```

## 더 사실적으로 나오게 하는 요령

스킬이 프롬프트를 만들 때 따르는 원칙입니다. 직접 수정할 때도 참고하세요.

- **칭찬하는 말 대신 구체적 사실을 씁니다.** `8k`, `masterpiece`, `hyperrealistic`, `stunning` 같은 말은 오히려 CG처럼 보이게 만듭니다.
- **광원은 하나로 정합니다.** 서로 다른 방향이나 시간대의 빛이 섞이면 가짜처럼 보입니다.
- **불완전한 부분을 한두 개 넣습니다.** 낡은 옷, 질퍽한 눈, 먼지 같은 것들입니다.
- **카메라를 쳐다보며 웃는 포즈는 피합니다.** 스톡 사진처럼 보이기 쉽습니다.
- **간판 글자는 비워 두지 말고 정확히 지정합니다.** 글자를 정하지 않으면 모델이 뜻 없는 가짜 한글을 채웁니다. 장소에 맞는 상호(예: `"대성철공"` / `"철구조물·용접·절단·가공"`)를 큰따옴표로 지정하고, 배경에 보일 세로 간판에도 짧은 상호를 붙입니다. "흐리게"나 "간판 없음"이라고 지시해도 모델이 가짜 글자를 그렸기 때문입니다. 그래도 남은 가짜 글자는 생성 후 편집 지시(예: `Change the text on the tall vertical sign on the right to "문래정밀". Keep everything else the same.`)로 고칩니다. 관광 안내판이나 영문 표지판은 넣지 않습니다.

## 리서치가 필요한 장면

`1970년대 서울 시장`, `반도체 클린룸`처럼 고증이 필요한 장면은 Claude가 먼저 조사합니다.

- 조사 전에 이미지의 용도와 고증을 얼마나 엄격하게 할지 먼저 묻습니다.
- 조사 결과 끝에는 **불확실성 지도**가 붙습니다. 확신이 낮은 부분, 지나치게 단순화했을 수 있는 부분, 판단을 바꿀 수 있는 추가 정보가 정리돼 있습니다.

## 파일 구성

```
image-skill/
├── README.md                                   ← 이 문서
└── .claude/skills/photoreal-image-prompt/
    ├── SKILL.md                                ← 스킬 본체 (진행 순서, 질문 규칙, 출력 형식)
    └── references/
        └── realism-cheatsheet.md               ← 카메라·조명·스타일 용어, AI 티 체크리스트, 모델별 메모
```

## 수정하는 방법

- 질문 순서나 출력 형식을 바꾸려면 `SKILL.md`를 수정합니다.
- 렌즈, 조명, 스타일 선택지에 쓸 어휘나 모델별 요령을 추가하려면 `references/realism-cheatsheet.md`를 수정합니다.
- 다른 프로젝트에서도 쓰고 싶다면 `photoreal-image-prompt` 폴더를 `~/.claude/skills/` 아래로 복사합니다.

## 모델별 차이 (관찰)

문래동 커플 프롬프트를 두 모델에 넣어 비교했습니다. Gemini는 프롬프트를 고쳐 가며 세 번 생성했습니다 (각 1장).

| | Gemini 기본 | Gemini 보정 1 (주 간판 지정 + "나머지 흐리게") | Gemini 보정 2 ("나머지 간판 없음") | ChatGPT 기본 |
|---|---|---|---|---|
| 주 간판 한글 | 가짜 한글 | 지정한 글자를 정확히 그림 | (잘린 화면이라 확인 못 함) | 맞는 한글을 스스로 채움 |
| 배경 간판 | 가짜 한글 | 지시 무시, 가짜 한글 | 지시 무시, 가짜 한글 | 영문 관광 안내판 추가 |
| 젖은 어깨 | 안 나옴 | 안 나옴 | 약하게 나옴 | 잘 나옴 |
| 색감·분위기 | 차분, 다큐 | 차분, 다큐 | 차분, 다큐 | 화려, 영화 같음 |

이어서 Gemini 대화창에서 편집 지시로 오른쪽 세로 간판을 "문래정밀"로 바꿔 보았습니다. 글자는 정확히 바뀌었고 나머지 이미지는 그대로였지만, 원래 간판이 더 길어서 맨 위에 이전 글자 한 자("어")가 남았습니다. 남은 글자는 한 번 더 편집해서 깨끗이 지웠습니다(나머지 이미지는 그대로 유지). 그래서 편집 문장에는 처음부터 글자 수와 "다른 글자 없음"을 함께 적습니다. 같은 대화창에서 다시 생성하면 편집으로 처리되므로, 새로 비교하려면 새 대화창을 쓰세요. 젖은 어깨는 Gemini에서 세 번 모두 거의 나오지 않았습니다.

그래서 스킬은 보일 만한 간판에 모두 짧은 글자를 지정하고, 남은 가짜 글자는 편집 문장으로 고치게 하며, 모델을 말하면 그 모델에 맞춘 보정 문장을 붙인 변형본을 함께 냅니다. 자세한 내용은 `references/realism-cheatsheet.md`의 "10. 모델별 메모"를 보세요.

## 알려진 한계

- 이 스킬로 만든 프롬프트를 실제 이미지 모델에 넣어 결과를 체계적으로 비교해 보지는 않았습니다.
- 모델별 메모(Midjourney 파라미터 등)는 모델이 업데이트되면 달라질 수 있습니다.
