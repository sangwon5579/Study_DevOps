FROM tomcat:11.0.11-jre21-temurin
#  작업 디렉토리 변경
WORKDIR /user/local/tomcat/webapps
# 작업 디렉터리 내 ROOT 디렉터리 생성
RUN [ "mkdir", "/ROOT"]
#  ROOT 디렉터리에 index.jsp 추가
ADD index.jsp ./ROOT
ENV TZ=Asia/Seoul
EXPOSE 8080
CMD ["catalina.sh", "run"]
