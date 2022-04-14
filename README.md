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

### Heroku 사이트 등록 필요 파일
- Procfile 
- runtime.txt
- requirements.txt

### docker (container) 관련
#### build 방법 
    git clone https://xxx.xxx.xx/  .
    sudo docker build --tag fa-basic .
    sudo docker images

#### 실행방법
    sudo docker run -d --name fastapi -p 8000:8000  -e DATABASE_URL=mysql\+pymysql:\/\/root:New1234\!\!\@34\.132\.246\.153:3306\/todoapp  fa-basic
    sudo docker run -d --name fastapi -p 8000:8000    fa-basic
