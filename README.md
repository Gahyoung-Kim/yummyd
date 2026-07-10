# Project_PWCode
# Project_PWCode

## 📖 프로젝트 소개
Project_PWCode는 React 기반의 웹 프론트엔드, Node.js 기반의 백엔드, 그리고 Python 기반의 머신러닝 서버(ML Server)로 구성된 현대적인 풀스택 웹 애플리케이션입니다.

## 🚀 주요 특징 및 아키텍처
이 프로젝트는 세 개의 주요 모듈로 분리되어 독립적으로 동작 및 통신합니다:
1. **Frontend**: 사용자 인터페이스 및 클라이언트 측 라우팅 처리
2. **Backend**: 주요 비즈니스 로직, 데이터베이스 연동, 사용자 인증(Authentication) 처리
3. **MLServer**: 머신러닝 모델 추론 및 데이터 분석을 위한 독립적인 API 서비스

## 🛠 기술 스택
### Frontend
- **Framework/Library**: React, Vite
- **Routing & Validation**: React Router DOM, Zod
- **HTTP Client**: Axios

### Backend
- **Environment**: Node.js
- **Framework**: Express.js (추정)
- **Database**: MySQL
- **Security**: Bcrypt (비밀번호 암호화), CORS

### MLServer
- **Environment**: Python
- **Architecture**: `api`, `core`, `services` 기반의 모듈화된 계층형 구조 (FastAPI 추정)
- **Machine Learning**: `ml_core`를 통한 모델 및 데이터 파이프라인 관리

## 📁 핵심 폴더 구조
```text
Project_PWCode/
├── backend/               # Node.js 백엔드 서버
│   ├── controllers/       # 요청 처리 및 응답 로직
│   ├── database/          # DB 연결 및 설정
│   ├── models/            # 데이터베이스 모델
│   └── routes/            # API 라우팅 계층
├── frontend/              # React 프론트엔드 (Vite)
│   ├── public/            # 정적 파일
│   └── src/
│       ├── assets/        # 이미지, 폰트 등 에셋 리소스
│       ├── components/    # 재사용 가능한 UI 컴포넌트
│       └── pages/         # 페이지 단위 컴포넌트
└── MLServer/              # 머신러닝 추론 API 서버
    ├── app/
    │   ├── api/           # ML API 엔드포인트
    │   ├── core/          # 핵심 설정 및 환경 변수
    │   ├── ml_core/       # 머신러닝 모델 및 전처리 로직
    │   ├── schemas/       # 데이터 검증 스키마 (e.g., Pydantic)
    │   └── services/      # ML 비즈니스 로직
    └── tests/             # 단위 및 통합 테스트
```

## ⚙️ 로컬 설치 및 실행 방법

각 모듈의 디렉토리로 이동하여 서버를 개별적으로 실행해야 합니다.

### 1. Backend 실행
```bash
cd backend
npm install
npm start   # 또는 node 설정된 진입점 파일 실행
```

### 2. Frontend 실행
```bash
cd frontend
npm install
npm run dev
```

### 3. MLServer 실행
```bash
cd MLServer
# 가상환경(venv 등) 생성 및 활성화 권장
pip install -r requirements.txt  # 의존성 설치
# 서버 실행 명령어 (예: uvicorn app.main:app --reload)
```

