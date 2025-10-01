# 베이스 이미지를 eclipse-temurin:21-jre-alpine-3.22로 지정
FROM eclipse-temurin:21-jre-alpine-3.22
# 작성자 레이블 생성
LABEL maintainer="cho123 <cho123@beyond.com>"
# 버전 레이블 생성
LABEL version="1.0"
# 이미지의 /root 디렉터리에 department-service-0.0.1-SNAPSHOT.jar 파일을 복사
COPY department-service-0.0.1-SNAPSHOT.jar /root
# 타임존 환경변수를 아시아/서울로 설정
ENV TZ=Asia/Seoul
ENV PROFILE=dev
EXPOSE 8088
# 작업 디렉터리를 /root로 변경
WORKDIR /root
# 컨테이너가 실행 시 department-service-0.0.1-SNAPSHOT.jar 파일을 실행하도록 설정
CMD ["java", "-jar", "department-service-0.0.1-SNAPSHOT.jar", "--spring.profiles.active=${PROFILE}" ]