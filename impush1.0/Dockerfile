FROM openjdk:8-jre-slim

ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

WORKDIR /app

COPY alpaca-push.jar /app/alpaca-push.jar

# 定义构建参数（默认为host.docker.internal）
ARG SERVER_ADDRESS=host.docker.internal

# 将构建参数的值赋给环境变量
ENV SERVER_ADDRESS=${SERVER_ADDRESS}

EXPOSE 8888

ENTRYPOINT ["java", "-Xms512m", "-Xmx1024m", "-jar", "alpaca-push.jar"]