FROM openjdk:8-alpine
RUN apk --update add wget tar bash
RUN wget http://apachemirror.wuchna.com/spark/spark-3.0.0-preview/spark-3.0.0-preview-bin-hadoop2.7.tgz
RUN tar -xzf spark-3.0.0-preview-bin-hadoop2.7.tgz && \
    mv spark-3.0.0-preview-bin-hadoop2.7 /spark && \
    rm spark-3.0.0-preview-bin-hadoop2.7.tgz
EXPOSE 8080
EXPOSE 7077
COPY start-master.sh /start-master.sh
COPY start-worker.sh /start-worker.sh
RUN chmod +x /*.sh
