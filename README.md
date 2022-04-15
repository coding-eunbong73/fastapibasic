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
    git clone https://github.com/coding-eunbong73/fastapibasic.git  .
    docker build --tag fastapi-eb:0.1 .
    docker images

#### 실행방법
    docker run -d --name fastapi -p 8000:8000  fastapi-eb:0.1
    docker run -d --name fastapi -p 8000:8000  -v dbdata:/code/data  fastapi:0.1
    docker run -d --name fastapi -p 8000:8000  -e DATABASE_URL=mysql\+pymysql:\/\/root:New1234\!\!\@localhost:3306\/todoapp  fastapi-eb:0.1

#### Confirm
    In Browser, http://[IP]:8000

#### Docker volume Confirm
    docker volume inspect dbdata
    docker volume ls
    docker exec fastapi-ui ls /code/data

### docker.io에 push
    docker login
    docker build -t eblee73/fastapi-eb:0.1 .
    docker push eblee73/fastapi-eb:0.1

### docker.io에 pull 받아 실행
    docker run -d --name fastapi -p 8000:8000  eblee73/fastapi-eb:0.1

    