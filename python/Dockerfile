# 1. Base Image: Python 가벼운 버전 사용
FROM python:3.9-slim

# 2. 작업 디렉토리 설정
WORKDIR /app

# 3. 의존성 파일 복사 및 설치
# (코드보다 먼저 복사해야 캐싱 효율이 좋습니다)
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# 4. 소스 코드 복사
COPY . .

# 5. 실행 명령어 (Uvicorn 실행)
# --host 0.0.0.0은 외부(호스트)에서 컨테이너에 접속하기 위해 필수입니다.
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]