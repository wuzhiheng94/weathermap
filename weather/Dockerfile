FROM swr.cn-north-4.myhuaweicloud.com/op_svc_cse/openjdk-x86_64:8-1.2.0

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

WORKDIR /home/apps/
ADD target/weather-1.0.0.jar .
ADD start.sh .
RUN echo version:1.0.2 > /home/apps/version.txt

ENTRYPOINT ["sh", "/home/apps/start.sh"]
