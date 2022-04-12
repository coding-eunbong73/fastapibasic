## 수행방법

### 가상환경 모듈 설치 및 가상환경 생성
pip install venv
python -m venv venv   ( 프로젝트내 venv라는 디렉토리 생성됨)

### virtualenv 활성화
./venv/Scripts/activate 실행

### 필수 라이브러리 설치
pip install -r requirements.txt

### virtual 환경구성 ( python 작업별 필요한 library가 달라서, 가상환경 구성하여 모듈 설치)

### 실행
uvicorn main:app --reload
