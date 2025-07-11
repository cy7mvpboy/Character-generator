# 🎨 캐릭터 생성기

Google AI Studio의 Gemini API를 활용하여 텍스트 설명이나 이미지를 기반으로 새로운 캐릭터 이미지를 생성하고, 캐릭터의 상세 정보를 만들어주는 웹 애플리케이션입니다.

## ✨ 주요 기능

- **텍스트 기반 캐릭터 이미지 생성**:
  - 자세한 텍스트 프롬프트를 입력하여 원하는 캐릭터 이미지를 생성할 수 있습니다.
  - `Imagen 3.0`, `Imagen 4.0`, `Gemini 2.0` 등 다양한 이미지 생성 모델을 선택할 수 있습니다.
  - `1:1`, `16:9`, `4:3` 등 다양한 이미지 비율을 선택하여 생성할 수 있습니다.
- **이미지 기반 캐릭터 특징 분석 및 생성**:
  - 기존 캐릭터 이미지를 업로드하면, Gemini Vision API가 이미지를 분석하여 특징을 텍스트로 설명해줍니다.
  - 분석된 텍스트를 기반으로 새로운 캐릭터 이미지를 생성하거나 기존 프롬프트를 보강할 수 있습니다.
- **캐릭터 정보 생성**:
  - 생성된 캐릭터의 특징(프롬프트)을 기반으로 이름, 성격, 배경 이야기 등 상세한 캐릭터 정보를 생성합니다.
- **편의 기능**:
  - 프롬프트 작성을 돕는 가이드라인과 다양한 스타일의 템플릿을 제공합니다.
  - 생성된 이미지와 캐릭터 정보를 쉽게 다운로드하거나 복사할 수 있습니다.

## 🚀 사용 방법

1. **Gemini API 키 발급**:
   - [Google AI Studio](https://aistudio.google.com/app/apikey)에 방문하여 Gemini API 키를 발급받습니다.
   - **참고**: 이미지 생성 기능을 사용하려면 Google Cloud 프로젝트에 유효한 [결제 계정](https://console.cloud.google.com/billing)이 연결되어 있어야 하며, [Vertex AI API](https://console.cloud.google.com/apis/library/vertexai.googleapis.com)가 활성화되어 있어야 합니다.
2. **API 키 입력**:
   - 애플리케이션 상단의 `Gemini API 키` 입력란에 발급받은 키를 붙여넣습니다.
3. **캐릭터 생성**:
   - **텍스트로 생성**:
     - `캐릭터 생성 가이드라인`을 참고하여 프롬프트 입력창에 원하는 캐릭터의 모습을 상세하게 묘사합니다. (영어로 작성 시 더 좋은 결과)
     - 원하는 `이미지 생성 모델`과 `이미지 비율`을 선택합니다.
     - `✨ 이미지 생성` 버튼을 클릭합니다.
   - **이미지로 생성**:
     - `이미지 업로드` 버튼을 클릭하여 분석할 이미지를 선택합니다.
     - 이미지 분석이 완료되면, 분석 결과를 `덮어쓰기`할지, 기존 프롬프트에 `추가`할지 선택합니다.
     - `✨ 이미지 생성` 버튼을 클릭합니다.
4. **캐릭터 정보 확인**:
   - 이미지 생성이 완료된 후, `✨ 캐릭터 정보 생성` 버튼을 클릭하면 해당 캐릭터의 상세한 설정(이름, 성격, 배경 등)이 생성됩니다.
   - `정보 복사` 버튼으로 생성된 정보를 클립보드에 복사할 수 있습니다.

## ✍️ 캐릭터 생성 가이드라인

효과적인 캐릭터 이미지를 생성하려면 명확하고 구체적인 프롬프트 작성이 중요합니다. 다음 가이드라인을 참고하여 최고의 결과물을 만들어보세요.

### 1. 기본 원칙

- **명확하고 구체적으로 작성하세요.**
  - **나쁜 예**: `사람`
  - **좋은 예**: `긴 빨간 머리를 가진 젊은 여성, 가죽 재킷을 입고 번화한 도시 거리에서 자신감 있게 서 있는 모습`
- **상세한 묘사를 사용하세요.**
  - `고요한`, `사려 깊은 표정`, `신비로운` 등 형용사와 부사를 활용하여 분위기와 스타일을 전달하세요.
- **반복적으로 개선하세요.**
  - 처음부터 완벽한 프롬프트를 만들기 어렵습니다. 초기 결과물을 보고 점진적으로 프롬프트를 수정하고 개선해나가세요.
- **행동 지향적인 동사로 시작하세요.**
  - `마법 지팡이를 높이 들고 휘날리는 로브를 입은 마법사의 전신 모습 생성`과 같이 명확한 동사로 시작하면 좋습니다.

### 2. 프롬프트 구조화

효과적인 프롬프트는 다음과 같은 핵심 요소로 구성됩니다.

- **주제 (Subject)**: `젊은 여성의 초상화`, `근육질의 전사`
- **배경 (Setting)**: `어두운 고대 성 홀`, `번화한 도시 거리`
- **스타일 (Style)**: `3D 이미지`, `일러스트레이션`, `사실주의`, `애니메이션`, `사이버펑크 2077 스타일`
- **분위기/표정 (Mood/Expression)**: `고요한`, `사려 깊은 표정`, `활기찬`
- **행동/포즈 (Action/Pose)**: `우아하게 서 있는`, `책을 들고 있는`
- **구도/조명 (Composition/Lighting)**: `클로즈업`, `와이드 샷`, `부드러운 빛`, `4k 해상도`

**프롬프트 형식**: 완전한 문장으로 작성하거나, 쉼표로 구분된 키워드 목록으로 구성할 수 있습니다.

- **문장 형식**: `해변에 앉아 햇살을 즐기는 고양이`
- **키워드 형식**: `고양이, 해변, 밝은 햇살, 즐거운 표정`

### 3. 고급 기법

- **가중치 부여 (Weighting)**: 특정 키워드를 강조하여 AI가 더 집중하도록 할 수 있습니다. (모델에 따라 사용법이 다를 수 있습니다.)
  - **예시**: `(((근육질 전사)))와 ((빛나는 푸른 눈))을 가진 캐릭터`
- **부정 프롬프트 (Negative Prompts)**: 원하지 않는 요소를 제외하여 이미지 품질을 높일 수 있습니다.
  - **일반적인 예시**: `worst quality, low quality, blurry, bad anatomy, deformed`
  - **캐릭터 예시**: `bad hands, missing legs, poorly drawn face`
- **참조 활용**: 특정 아티스트, 스타일, 카메라 앵글, 조명 등을 명시하여 원하는 결과물에 더 가깝게 만들 수 있습니다.
  - **해상도**: `4k`, `8k`
  - **카메라 앵글**: `클로즈업`, `와이드 샷`, `공중 샷`
  - **조명**: `부드러운 빛`, `극적인 조명`
  - **아티스트/스타일**: `반 고흐 스타일`, `픽사 스타일`

### 4. 캐릭터 일관성 유지

여러 이미지에서 동일한 캐릭터를 유지하려면 다음 전략을 활용해 보세요.

- **상세하고 일관된 프롬프트 사용**: 수염 길이, 눈 색깔, 의상 등 세부 사항을 모든 프롬프트에서 동일하게 유지하세요.
- **배경과 캐릭터 분리**: 캐릭터 생성에 집중한 후, 다른 프롬프트로 배경을 생성하여 합성하는 것도 좋은 방법입니다.
- **표정과 행동만 변경**: 기본 프롬프트는 유지하되, 캐릭터의 표정이나 행동과 관련된 부분만 수��하여 일관성을 높일 수 있습니다.

## 🛠️ 기술 스택

- **Frontend**: HTML, CSS, JavaScript
- **AI**: Google Gemini API (Imagen, Gemini Vision)
- **Styling**: Tailwind CSS (CDN)
