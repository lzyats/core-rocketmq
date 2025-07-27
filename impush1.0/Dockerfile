FROM openjdk:8-jre-slim

ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

WORKDIR /app

COPY alpaca-push.jar /app/alpaca-push.jar

EXPOSE 8888

ENTRYPOINT ["java", "-Xms512m", "-Xmx1024m", "-jar", "alpaca-push.jar"]