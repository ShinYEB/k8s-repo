# 1. Base Image 선택 (Java 17 버전의 가벼운 Alpine Linux 기반)
FROM eclipse-temurin:17-jdk-alpine

# 2. 작업 디렉토리 설정
WORKDIR /app

# 3. 빌드된 JAR 파일을 이미지 내부로 복사
# target/*.jar는 빌드된 jar 파일을 의미하며 app.jar라는 이름으로 복사합니다.
COPY target/*.jar app.jar

# 4. 컨테이너 실행 시 실행될 명령어
ENTRYPOINT ["java", "-jar", "app.jar"]