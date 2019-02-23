FROM java:8-jre-alpine
# 设置环境变量
ENV TZ=Asia/Shanghai
# 设置时区
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
#VOLUME /tmp
ENV PARAMS=""
ADD dubbo-admin-0.1.jar dubbo-admin-0.1.jar
#ENTRYPOINT ["java","-jar","/dubbo-admin-0.1.jar","-Djava.security.egd=file:/dev/./urandom"]
ENTRYPOINT ["sh","-c","java -jar /dubbo-admin-0.1.jar --$PARAMS"]