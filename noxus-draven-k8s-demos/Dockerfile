# 基础镜像
FROM openjdk:8-jdk-alpine
# 作者（可选）
MAINTAINER duhyper
# 删除无用组件 优化容器体积（可选）
# RUN rm -rf /var/lib/apt/lists/*
# 创建jar包存放目录
RUN mkdir -p /usr/local/duhyper
# 获取pom文件中build参数
ARG JAR_FILE
# copy当前工程jar包至容器内
COPY ${JAR_FILE} /usr/local/duhyper/app.jar
# 运行jar包
ENTRYPOINT ["java","-jar","/usr/local/duhyper/app.jar"]