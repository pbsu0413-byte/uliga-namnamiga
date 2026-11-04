---
mode: "agent"
description: "4단계: Azure Cloud (Static Web Apps / App Service) 배포 전 빌드 점검 및 설정 파일 생성"
---
프로젝트를 **Azure Cloud**에 배포하려고 해. 아래 항목을 순서대로 점검하고 필요한 설정 파일을 만들어 줘:

1. `.gitignore` 파일 점검 (`.env`, `node_modules`, `.next`, `__pycache__`, `.venv` 등이 반드시 제외되었는지 확인)
2. 프로덕션 빌드 또는 실행 테스트를 수행하여 타입 에러, 문법 에러, 누락된 의존성(`package.json` 또는 `requirements.txt`)이 없는지 확인하고 모두 수정해 줘.
3. 배포 타겟에 맞는 설정 파일 생성:
   - 프론트엔드/Next.js/React인 경우: Azure Static Web Apps용 `staticwebapp.config.json` 생성
   - Python(Streamlit/FastAPI) 또는 서버 앱인 경우: `requirements.txt` 최신화 및 Azure App Service용 `startup.sh` 생성
4. 배포 후 Azure Portal 환경 변수에 등록해야 할 목록을 정리해 줘.
