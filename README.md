# TAVE 심화 프로젝트 - 퍼스널 컬러 기반 패션 아이템 추천 시스템

## 프로젝트 소개
웹 브라우저와 Streamlit을 활용하여 사용자의 이미지를 분석하고 퍼스널 컬러를 진단하여 최적의 패션 아이템을 추천하는 시스템입니다.

## 주요 기능
- **이미지 기반 퍼스널 컬러 진단**
- **진단 결과에 따른 맞춤형 패션 아이템 추천**
- **사용자 추천 이력 관리**

## 기술 스택

| 구분       | 사용 기술                |
|------------|--------------------------|
| Frontend   | Streamlit                |
| Backend    | FastAPI                  |
| Database   | MySQL                    |
| Image Processing | OpenCV, PIL        |
| Model      | PyTorch, scikit-learn    |

## 시스템 구성도
```
Client <-> Streamlit Frontend <-> FastAPI Backend <-> MySQL Database
```

## 설치 및 실행

### 필수 요구사항
- Python 3.8+
- MySQL 8.0+
- 가상환경 관리자

### 설치 방법
```bash
# 저장소 클론
git clone https://github.com/TAVE-Research/personal-color-recommendation.git

# 가상환경 설정
python -m venv venv
source venv/bin/activate  # Windows: .\venv\Scripts\activate

# 의존성 설치
pip install -r requirements.txt

# 환경변수 설정
# .env 파일을 열어 필요한 설정값 입력
```

### 실행 방법
```bash

# FastAPI 서버 실행
uvicorn app.main:app --reload

# Streamlit 앱 실행
streamlit run frontend/main.py
```

## 프로젝트 구조
```
.
├── app/
│   ├── api/            # API 라우터
│   ├── core/           # 설정 및 상수
│   ├── models/         # 데이터베이스 모델
│   └── services/       # 비즈니스 로직
├── frontend/
│   ├── pages/          # Streamlit 페이지
│   └── components/     # UI 컴포넌트
├── tests/              # 테스트 코드
├── alembic/            # DB 마이그레이션
├── requirements.txt    
└── README.md
```

## 개발 가이드
- **코드 스타일:** PEP 8
- **커밋 메시지:** Conventional Commits
- **API 문서:** FastAPI Swagger UI (/docs)

## 라이센스
MIT License

## 팀원
- **팀장:** 기은서
- **팀원:** 최정아
- **팀원:** 이승희
- **팀원:** 최윤성
