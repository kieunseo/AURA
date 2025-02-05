# 퍼스널 컬러 기반 패션 아이템 추천 시스템 - TAVE 후반기 프로젝트 우수상🏆

## 프로젝트 소개
웹 브라우저와 Streamlit을 활용하여 사용자의 이미지를 분석하고 퍼스널 컬러를 진단하여 최적의 패션 아이템을 추천하는 시스템입니다.

https://github.com/user-attachments/assets/26428d8f-9508-4c73-bb6f-67ab66d90fe8

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
git clone https://github.com/kieunseo/AURA.git

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
streamlit run streamlit/home.py
```

## 프로젝트 구조
```
├── app/
│   ├── sql_app/           
│       ├── crud.py        # CRUD 로직
│       ├── models.py      # 데이터베이스 모델 정의
│       ├── schemas.py     # Pydantic 스키마 정의
│       ├── database.py    # DB 연결 설정
│   ├── item_recommendation.py  # 아이템 추천 로직
│   ├── personal_color_classifier.py  # 퍼스널 컬러 분류기
│   ├── shape_predictor_68_face_landmarks.dat  # 얼굴 랜드마크 모델
│   └── main.py            # FastAPI 메인 실행 파일
├── streamlit_app/
│   ├── pages/             
│       ├── 1_Personal_Color.py  # 퍼스널 컬러 분석 페이지
│       ├── 2_Item_Recommendation.py  # 아이템 추천 페이지
│       ├── images/              # 이미지 폴더
│   ├── Home.py            # Streamlit 메인 페이지
│   ├── homepgim.jpg       # 홈 이미지
├── prsonal_color_dataset/ # 연예인 얼굴 이미지
│   ├── images/          
│   └── labels.csv
├── fashoin_data/ # musinsa crawling
│   ├── crawling_code/          
│   └── data/ # 크롤링된 데이터
├── sql_dataset/ # fashion data 전처리 및 MySQL 적재
│   ├── csv_sql_upload.ipynb       # CSV 데이터를 SQL에 업로드하는 코드
│   ├── fashion_data_preprocessing.ipynb  # 패션 데이터 전처리 코드
│   ├── fashion_data.csv           # 최종 데이터
│   ├── data.csv                   # 전처리 데이터
│   └── data_original.csv          # 원본 데이터
├── notebook/             
│   ├── personal_visualization.ipynb  # 데이터 시각화 노트북    
├── docs/                          
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
- **팀원:** 최정아, 이승희, 최윤성

## 수상 내역
**후반기 프로젝트 우수상**
- 주최: TAVE 학술동아리

