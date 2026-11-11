# Realism Cheatsheet

4·5단계 선택지를 만들 때, 그리고 최종 프롬프트를 점검할 때 참고한다.

## 목차
1. 샷 크기
2. 렌즈(초점거리)와 효과
3. 조리개·심도
4. 카메라 높이·앵글·움직임
5. 조명: 광원 × 방향 × 질감
6. 사진 장르(스타일) 문구
7. 색감 팔레트
8. 사실감 디테일
9. "AI 티" 체크리스트
10. 모델별 메모
11. 간판·현지 글자
12. 충돌 점검 예시

---

## 1. 샷 크기
| 영문 | 의미 | 언제 |
|---|---|---|
| extreme close-up | 눈·손 등 일부 | 질감 강조 |
| close-up | 얼굴/어깨 위 | 감정, 피부 결 |
| medium close-up | 가슴 위 | 인터뷰·인물 |
| medium shot | 허리 위 | 동작 + 일부 환경 |
| medium wide / full shot | 전신 | 자세·옷차림 전체 |
| wide shot | 인물 + 넓은 환경 | 장소의 맥락 |
| establishing shot | 장소 위주 | 공간 소개 |

## 2. 렌즈(초점거리)
| 렌즈 | 효과 | 트레이드오프 |
|---|---|---|
| 24mm | 넓은 화각, 원근 과장 | 가장자리 왜곡, 가까운 얼굴이 커 보임 |
| 35mm | 다큐·스트리트 표준, 환경 포함 | 인물 강조는 약함 |
| 50mm | 사람 눈과 비슷한 시야, 가장 무난 | 극적인 효과 적음 |
| 85mm | 인물 사진 표준, 배경 압축·흐림 | 환경 정보 감소 |
| 135mm+ | 강한 압축, 원거리 몰래 찍은 느낌 | 공간감 납작 |
| 100mm macro | 근접 질감 | 피사체 일부만 |

## 3. 조리개·심도
- `shallow depth of field, f/1.8` — 배경 흐림, 인물 분리. 과하면 합성처럼 보임.
- `moderate depth of field, f/4` — 인물 선명 + 배경 형태 유지. 다큐에 무난.
- `deep focus, f/8–f/11` — 전부 선명. 풍경·건축·현장 기록.

## 4. 카메라 높이·앵글·움직임
- eye level (가장 자연스러움) / slightly low angle / high angle / overhead (top-down)
- static camera on tripod / handheld (살짝 기울어진 프레임) / over-the-shoulder
- 비디오 모델이 아니면 "camera movement"는 정지 혹은 handheld 느낌 정도로만.

## 5. 조명: 광원 × 방향 × 질감
**광원:** window light, overcast daylight, golden hour sun, midday sun, overhead fluorescent tubes, sodium-vapor street lamps, tungsten desk lamp, neon signage, screen glow, single bare bulb, candle
**방향:** from the left/right, backlit, side-lit, top-down, from behind the camera
**질감:** soft and diffused / hard with crisp shadows / mixed color temperatures (warm interior vs. cool daylight)

좋은 예: `Overcast daylight through a large north-facing window on the right, soft shadows, slightly cool tone.`
나쁜 예: `cinematic lighting, dramatic, beautiful light`

## 6. 사진 장르(스타일) 문구
- `photorealistic documentary photography` — 현장 기록, 연출 최소
- `candid street photography` — 지나가다 포착한 순간
- `editorial portrait photography` — 잡지 인물, 정돈된 연출
- `amateur smartphone snapshot` — 가장 "진짜 같은" 결과를 원할 때 강력. 약간의 노이즈·평범한 구도
- `photojournalism, 35mm film` — 거친 입자, 시대감
- `commercial product photography` — 깨끗한 연출(제품용)

## 7. 색감 팔레트
muted industrial palette, natural colors, desaturated earth tones, warm tungsten tones, cool blue-hour palette, faded film colors (Kodak Portra 400 / Fujifilm Superia 느낌), high-contrast black and white

## 8. 사실감 디테일 (1~2개만)
- 사람: natural skin texture with visible pores, slight under-eye shadows, flyaway hairs, creased clothing
- 공간: scuffed floor, dust in the light beam, fingerprints on glass, worn edges, cable clutter
- 사진 자체: subtle film grain, slight motion blur on hands, mild lens vignetting, natural sensor noise in shadows

## 9. "AI 티" 체크리스트
최종 프롬프트를 내기 전에 확인:
- [ ] 칭찬 형용사(8k, masterpiece, stunning, hyperrealistic)를 쓰지 않았다
- [ ] 광원이 하나로 일관되고 시간대와 맞는다
- [ ] 피사체가 카메라를 보고 웃는 스톡 포즈가 아니다 (의도한 경우 제외)
- [ ] 배경에 실제 장소의 흔적이 1~2개 있다
- [ ] 불완전함이 1~2개 있다 (과하지 않게)
- [ ] 렌즈·조리개 조합이 물리적으로 가능하다
- [ ] 간판이 보이면 주 간판 하나의 글자를 큰따옴표로 지정했고, 보일 만한 배경 간판(특히 세로 간판)에도 짧은 상호를 지정했다 — 지정하지 않은 글자는 "흐리게"나 "없음"이라고 해도 가짜 한글이 된다
- [ ] 장면에 있을 이유가 없는 글자(관광 안내판, 영문 표지판)를 넣지 않았다
- [ ] 손이 화면에 크게 나오면 손의 동작을 구체적으로 적었다 ("one hand resting on the rail")
- [ ] 핵심 디테일이 다른 선택(옷 색, 빛, 거리, 방향)과 함께 있을 때 실제로 보이는지 점검했다 (12장)

## 10. 모델별 메모
사용자가 모델을 지정했을 때만 변형본에 반영한다. 모델 업데이트가 잦으므로 확신은 낮게 갖는다.

- **GPT Image (ChatGPT):** 서술형 문단을 잘 따른다. 장면 → 피사체 → 디테일 → 용도 → 제약 순으로 쓰면 안정적. 비율은 문장으로("vertical 4:5 composition").
  - *관찰 (문래동 커플 프롬프트, 1회 비교):* 간판 글자를 지정하지 않았는데도 업종에 맞는 그럴듯한 한글 간판("대성철공 / 철구조물·용접·절단·가공")을 스스로 채웠다. 동작 디테일(우산 기울이기, 젖은 어깨)도 반영했다. 대신 요청하지 않은 연출 요소(영문 관광 안내판, 용접 불꽃, 강한 반사광)를 더해 화려하고 영화 같은 쪽으로 기우는 경향이 있었다.
  - *보정:* 변형본에 `No English signage, no added props beyond those described. Muted, understated light — not cinematic.` 같은 절제 문장을 붙인다.
- **Gemini / Imagen (Nano Banana):** Google 공식 가이드는 subject · context · style 구조를 권한다. 렌즈·카메라 용어를 잘 따른다. 문장형 서술 권장.
  - *관찰 (같은 프롬프트, 1회 비교):* 색감과 빛이 차분해서 다큐 사진에 더 가까웠다. 그러나 지정하지 않은 간판은 뜻 없는 가짜 한글("물알연돈사" 등)로 채웠고, 동작 디테일(우산 기울이기, 젖은 어깨)은 약하게 반영했다.
  - *관찰 2 (간판 지정 + 동작 강조 보정판, 1회):* 큰따옴표로 지정한 "대성철공 / 철구조물·용접·절단·가공"을 **정확히** 그렸다. 하지만 `All other signs … out of focus and unreadable`은 지키지 않았다 — 뒤쪽 세로 간판들이 선명한 가짜 한글로 나왔고, 주 간판 아래에도 흐릿한 가짜 글자 줄이 생겼다. 젖은 어깨는 따로 강조했는데도 두 번 연속 나오지 않았다. 차분한 다큐 색감과 대화하는 시선은 잘 따랐다.
  - *관찰 3 (나머지 간판 "없음" 보정판, 1회):* `The rest of the alley has no other signs, only closed metal shutters` 지시도 무시하고 뒤쪽 세로 간판 두 개에 가짜 한글("어설말공사" 비슷한 글자)이 나왔다. 젖은 어깨는 데님 위에 약한 물기 정도로만 보였다.
  - *관찰 4 (편집 지시 ①, 배경 간판 지정 재생성 ②):* 같은 대화창에서 이어서 했더니 ①·②가 거의 같은 이미지로 나왔다 — Gemini가 ②도 이전 이미지의 편집으로 처리한 것으로 보인다. 결과: 오른쪽 세로 간판이 "문래정밀"로 **정확히** 바뀌었고 나머지는 그대로 유지됐다(편집 성공). 하지만 원래 간판이 더 길어서 맨 위에 이전 글자 한 자("어")가 남았다. 왼쪽에 지정한 "삼화금속"은 그 자리에 간판이 없어서 아예 나오지 않았다. 멀리 있는 작은 간판들과 주 간판 아래 줄은 흐릿한 가짜 글자로 남았지만 거의 눈에 띄지 않는다. 젖은 어깨와 우산 기울이기는 3회 연속 나오지 않았다.
  - *보정:* ① 간판 글자는 큰따옴표로 지정한다(효과 확인됨). ② 배경 세로 간판에도 짧은 상호를 지정한다 — 흐리게·없애기는 둘 다 실패했다. 편집 때는 `The sign shows only the four characters "문래정밀", filling the whole sign from top to bottom; no other characters.`처럼 **글자 수와 "다른 글자 없음"**을 함께 적어 남는 글자를 막는다. 남았다면 `Remove the extra character "어" at the top of the tall vertical sign on the right, so the sign shows only "문래정밀". Keep everything else in the image exactly the same.`로 한 번 더 고친다 — *관찰 5:* 이 후속 편집으로 남은 글자가 깨끗이 지워졌고, "문래정밀"이 간판을 꽉 채웠으며, 나머지 이미지는 그대로였다(1회). 즉 Gemini는 **"생성 → 간판 글자 편집 → 남은 글자 제거"** 2~3번의 편집으로 간판 문제를 해결할 수 있었다. ③ 새로 생성해서 비교하려면 **새 대화창**에서 한다 — 같은 대화에서는 편집으로 처리된다. ④ 우산 기울이기·젖은 어깨처럼 작은 동작 결과는 Gemini에서 기대하지 않는다. 꼭 필요하면 ChatGPT를 쓰거나 편집으로 따로 요청한다. ③ 비울 곳은 부정문 대신 긍정형으로 묘사한다. ④ 남은 가짜 글자는 생성 후 편집 지시로 고친다. ⑤ 주 간판 아래 여백은 `nothing written below the sign`으로 막는다. ④ 젖은 어깨처럼 작은 물리적 결과는 Gemini가 잘 따르지 않으므로, 꼭 필요하면 눈에 보이는 모양으로 쓴다(`a dark wet patch with beaded raindrops on the shoulder of his denim jacket`). 그래도 안 나오면 후편집이나 다른 모델을 권한다.
- **Midjourney:** 끝에 파라미터를 붙인다 — 사실감에는 `--style raw`, 비율 `--ar 3:2`, 네거티브는 `--no text, watermark`. 문장은 짧게, 핵심 먼저.
- **Flux / Stable Diffusion 계열:** 앞쪽 단어의 영향이 크다 — 피사체와 사진 장르를 앞에 둔다. SD 계열은 네거티브 프롬프트 칸을 별도로 활용.
- **한글 렌더링:** GPT Image는 지정하지 않아도 맥락에 맞는 한글을 그렸다. Gemini는 지정한 한글은 정확히 그렸지만, 지정하지 않은 간판은 "흐리게"나 "간판 없음" 지시가 있어도 가짜 한글로 채웠다. 구형 SD·일부 Flux 모델은 한글이 자주 깨진다. 어떤 모델이든 **보일 만한 간판은 모두 짧게 지정하고, 남은 가짜 글자는 편집으로 고치는 것**이 지금까지 가장 안전한 기본값이다. 위 관찰은 각 1장 비교라서, 결과가 다르게 나오면 이 메모를 고친다.

## 11. 간판·현지 글자

간판은 "이곳이 실제 장소"라는 가장 강한 신호다. 뜻 없는 가짜 한글은 가장 강한 "AI 신호"다. 그래서 비워 두지 말고 **지정**한다.

### 프롬프트에 쓰는 형식
```
A faded white sheet-metal sign above the workshop reads "대성철공" in large black Korean letters,
with a smaller line below reading "철구조물·용접·절단·가공". Other signs along the alley are out of focus and unreadable.
```
- 글자는 큰따옴표 안에 **정확한 한글**로. 영문 번역이나 로마자를 같이 쓰지 않는다(모델이 둘 다 그리려 한다).
- 주 간판 1개 + 보조 설명 1줄까지. 글자가 많을수록 오류가 늘어난다.
- 위치(above the doorway, on the shutter), 크기(large/small), 색(black on white), 물성(painted sheet metal, acrylic lightbox)을 함께 적는다.
- **배경 간판에도 짧은 글자를 지정한다.** Gemini에서 "흐리게"(`out of focus and unreadable`, 1회)와 "간판 없음"(`no other signs, only closed shutters`, 1회)은 모두 무시되고 세로 간판에 가짜 한글이 나왔다. 한국 골목은 세로 돌출 간판이 모델의 강한 기본값이라 지우기 어렵다. 대신 이름을 붙여 준다:
  ```
  Further down the alley, a tall vertical sign on the right reads "문래정밀",
  and a smaller vertical sign on the left reads "삼화금속".
  ```
- **부정문 대신 긍정형으로 채운다.** "no signs"는 간판이라는 단어를 넣어 오히려 간판을 부를 수 있다. 비워 둘 곳은 실제로 있는 것으로 묘사한다: `the upper floors are plain cement walls with small windows and air-conditioner units`.
- 주 간판 아래나 옆에 글자가 생기지 않게 `nothing else written on or below the sign`을 덧붙인다.
- **마지막 수단은 편집이다.** Gemini·ChatGPT 모두 생성된 이미지를 대화로 고칠 수 있다. 가짜 글자가 남으면:
  ```
  Change the text on the tall vertical sign on the right to "문래정밀".
  Keep everything else in the image exactly the same.
  ```
  Gemini에서 이 편집은 글자를 정확히 바꾸고 나머지를 그대로 유지했다(1회). 단, 원래 간판이 더 길면 이전 글자가 일부 남으므로 `only these four characters, filling the whole sign; no other characters`를 덧붙인다. 간판이 없는 자리에 새 간판을 지정하면 무시될 수 있다 — 편집은 **이미 있는 간판의 글자를 바꾸는 용도**로 쓴다.

### 상호 작명 패턴 (한국)
실존 업체명을 그대로 쓰지 말고 아래 패턴으로 지어낸다.
| 업종 | 상호 패턴 | 보조 설명 예 |
|---|---|---|
| 철공소·금속 | 대성철공, 삼화금속, 문래정밀, 동양철강, 한일용접 | 철구조물·용접·절단·가공 / 선반·밀링 / 각파이프·철판 |
| 시장 노점·상회 | 영희상회, 제일청과, 부산수산, 할머니 야채 | 산지직송 / 국산 / 도매·소매 |
| 식당 | 원조 ○○집, ○○식당, 이모네 | 백반·찌개 / 24시 |
| 철물·공구 | 대한철물, 신흥공구 | 철물·공구·전기자재 |
| 세탁·수선 (동네 개인점) | 명동세탁, 솜씨수선 | 세탁·수선 |
| 새로 들어선 카페·공방 | 짧은 한글/영문 혼용 이름 (예: "작업실 쇠", "공방 문") | 거의 없음 |
- 오래된 업종일수록 **두 글자 지명·길한 한자어 + 업종명**(대성, 삼화, 동양, 제일, 한일 + 철공/상회/정밀).
- 같은 골목에 비슷한 업종 간판이 줄지어 있는 것이 자연스럽다(철공소 옆 철공소).

### 간판 물성 어휘 (시대감)
- 1970~90년대 업소: `faded white sheet-metal sign with hand-painted black letters, rust streaks at the edges`
- 2000년대 상가: `acrylic lightbox sign with red and blue letters, slightly yellowed`
- 최근 공방·카페: `small minimalist sign, thin sans-serif letters` — 오래된 골목에서는 이런 간판이 한두 개 섞일 때만 자연스럽다.

### 피할 것
- 관광 안내판, 영문 방향 표지(예: "Mullae-dong Art Village →") — 실제 골목에 거의 없고, 사진을 연출된 관광 홍보물처럼 만든다. 사용자가 원할 때만.
- 브랜드 로고(운동화·옷 등)를 크게 — 실제 사진에도 있지만 모델이 틀리게 그리면 눈에 띈다. 필요 없으면 `no visible brand logos`.
- 간판 여러 개에 모두 긴 글자 지정 — 주 간판만 상호+설명, 배경 간판은 상호만 짧게(2~4자).

## 12. 충돌 점검 예시

단계별로 따로 고른 선택이 합쳐져 핵심 디테일을 가리는 경우다. 최종 출력 전에 확인한다.

| 핵심 디테일 | 충돌하는 선택 | 왜 안 보이나 | 고치는 방법 |
|---|---|---|---|
| 젖은 어깨·옷 | 어두운 데님·검은 옷 + 해 질 녘/밤 | 어두운 천은 젖어도 조금 더 어두워질 뿐 | 옷을 밝은 회색·베이지로, 또는 `beaded raindrops on the shoulder`처럼 빛나는 물방울로 표현 |
| 우산 기울이기 | 정면 클로즈업, 우산이 프레임 밖 | 우산 각도가 화면에 안 들어옴 | 우산 전체가 보이는 풀샷, `canopy centered over her head, not his` |
| 표정·시선 | 뒷모습 구도, 강한 역광 | 얼굴이 안 보이거나 실루엣이 됨 | 3/4 뒷모습에 옆얼굴 지정, 또는 얼굴 쪽에 보조광 |
| 피부 결·주름 | 와이드 샷, 먼 거리 | 크기가 너무 작아 안 보임 | 미디엄 샷 이상으로, 또는 디테일을 빼기 |
| 손 동작(끈 묶기, 뚜껑 열기) | 손이 몸·소품에 가림, 뒷모습 | 손이 카메라 쪽을 향하지 않음 | 카메라 방향에서 손이 보이는 앵글 지정 |
| 간판 글자 | 얕은 심도(f/1.4~1.8) + 간판이 배경 | 흐려져 글자가 뭉개짐 → 가짜 글자처럼 보임 | 간판을 피사체와 비슷한 거리에 두거나 f/4 이상 |
| 빗줄기·눈송이 | 순광, 밝은 배경 | 뒤에서 빛을 받아야 보임 | 광원을 뒤쪽에 두는 역광, 어두운 배경 |
| 김·연기 | 밝은 배경, 정면광 | 대비가 없음 | 어두운 배경 + 측광·역광 |
| 흰 옷의 얼룩·질감 | 흰 벽 배경, 과노출 | 배경과 섞임 | 배경 톤을 다르게 |

추가로 확인할 것:
- **인과관계로만 쓴 디테일** — "기울였고, 그래서 젖었다"보다 결과의 모습 자체를 쓴다.
- **좌우가 애매한 표현** — "바깥쪽 어깨", "반대쪽 손"은 `his left shoulder, the one away from her`처럼 카메라 기준 좌우나 관계로 특정한다.
- **모델별 약점** — 10장의 모델별 메모에서 약하다고 적힌 디테일이면(예: Gemini의 작은 동작 결과) 사용자에게 한 줄 알린다.
