# 베이스 이미지를 eclipse-temurin:21-jre-alpine-3.22로 지정
FROM eclipse-temurin:21-jre-alpine-3.22
# 작성자 레이블 생성
LABEL maintainer="cho123 <cho123@beyond.com>"
# 버전 레이블 생성
LABEL version="1.0"
# 이미지의 /root 디렉터리에 university-0.0.1-SNAPSHOT.jar라는 파일을 복사
COPY university-0.0.1-SNAPSHOT.jar /root
# 타임존 환경변수를 Asia/Seoul로 설정
ENV TZ=Asia/Seoul
# 이미지에서 8080 포트를 노출
EXPOSE 8080
# 작업 디렉토리를 /root 로 변경
WORKDIR /root
# 컨테이너가 실행 시 university-0.0.1-SNAPSHOT.jar 파일을 실행하도록 설정
CMD [ "java", "-jar", "university-0.0.1-SNAPSHOT.jar" ]