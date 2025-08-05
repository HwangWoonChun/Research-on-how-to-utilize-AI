
# AI 활용 1단계 정리 (LLM + Prompt + API 등)

## LLM 개념
- **Large Language Model**: 대규모 텍스트 데이터를 학습한 AI 언어 모델 (예: GPT, Claude, Mistral)
- **동작 원리**: 사용자의 질문을 받아 확률적으로 가장 자연스러운 응답을 생성

### 기억해야 할 개념
- **토큰**: 단어 단위 분해, 영어는 4자가 보통 한 토큰. 한글은 인코딩 방식으로 인해 처리량이 영어에 비해 두 배.
- **Context window**: 모델이 한 번에 이해 가능한 입력 길이 범위
- **temperature**: 창의성과 일관성의 균형 조절 (0에 가까울수록 일관, 높을수록 창의적)
- **top-p**: 누적 확률 기반 단어 선택 (nucleus sampling)
- **top-k**: 선택 가능한 후보 단어 개수 제한
- **embedding**: 문장이나 단어를 수치 벡터로 변환

---

## Prompt Engineering
- **Prompt란**: AI에게 어떤 식으로 질문할지를 정하는 입력 지문
- **중요성**: 같은 질문도 프롬프트 구성에 따라 응답 품질이 크게 달라짐

### 핵심 기법
- 명확하게 말하기
- 역할 지정: `You are a senior iOS engineer`
- 예시 추가: 길든 짧든 (few-shot learning)
- 제약 조건 부여: 출력 형식, 문체, 글자 수 등

---

## 주요 OpenAI API
- **제공 기능**: GPT, DALL·E, Whisper, Embedding 등
- **기본 호출 방식**: REST API, Python/Node SDK, curl 등

### 실무 적용 예시
- GPT 요약 기능
- GitHub PR 리뷰 요약 및 코멘트 자동 생성
- 유사도 기반 검색 (Embedding + Vector DB)

### 요금 체계
- **토큰 기반 과금**: prompt 토큰 + completion 토큰 사용량 기준

---

## 노코드/로우코드 도구
- **Flowise**: GPT 기반 워크플로우 설계 (노션 스타일 인터페이스)
- **LangChain (UI)**: 코드 없이 LLM + DB 파이프라인 구성
- **Dust, Cognosys**: 챗봇, 요약기, 멀티 에이전트 구현 가능
- **Zapier AI, Make + OpenAI**: 구글 시트 → 요약 → 메일 자동 전송 등 업무 자동화

---

## 이미지/음성 기반 AI 도구
- **DALL·E**: 텍스트 → 이미지 생성
- **Whisper**: 음성 → 텍스트 전사
- **ElevenLabs, PlayHT**: 텍스트 → 음성 합성 (AI 보이스)
- **Runway ML**: 동영상 편집, 합성, 배경 제거 등 다양한 크리에이티브 기능

