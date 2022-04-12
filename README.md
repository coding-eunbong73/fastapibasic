## 수행방법

### 가상환경 모듈 설치 및 가상환경 생성
    pip install venv
    python -m venv venv    ( venv라는 디렉토리 생성됨 )
- 작업별 필요 library가 달라 가상환경 구성하여 작업

### virtualenv 활성화 및 필수 라이브러리 설치
    ./venv/Scripts/activate 실행
    pip install -r requirements.txt

### 실행
    uvicorn main:app --reload
