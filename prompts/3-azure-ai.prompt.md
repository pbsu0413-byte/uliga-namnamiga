---
mode: "agent"
description: "3단계: Azure OpenAI API 연동 및 무중단 데모 Fallback(시뮬레이션) 구현"
---
현재 프로젝트에 **Azure OpenAI API**를 연동해서 핵심 AI 기능을 완성해 줘.

필수 요구사항:
1. `.env.example`의 환경 변수 키를 사용해 Azure OpenAI를 연결해 줘:
   - `AZURE_OPENAI_ENDPOINT`
   - `AZURE_OPENAI_API_KEY`
   - `AZURE_OPENAI_DEPLOYMENT_NAME`
   - `AZURE_OPENAI_API_VERSION`
2. 청도군 도메인 지식이 담긴 System Prompt를 구성해 사용자의 입력에 따라 맞춤형 결과(구조화된 카드 또는 스트리밍 응답)를 생성하도록 연결해 줘.
3. **[핵심] 무중단 Fallback 모드**: 만약 `.env`에 API 키가 아직 없거나 네트워크/API 호출 에러가 발생하더라도 절대 에러가 나지 않고, 자연스러운 로딩 후 **고품질 청도군 맞춤형 AI 시뮬레이션 결과**를 반환하도록 `try / catch` Fallback 로직을 반드시 함께 구현해 줘.
4. 화면에서 원클릭으로 테스트해 볼 수 있는 **'추천 예시 프롬프트 버튼 3개'**를 입력창 위에 배치해 줘.
