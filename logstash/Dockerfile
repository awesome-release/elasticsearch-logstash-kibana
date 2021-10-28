FROM logstash:7.8.0

ENV discovery.seed_hosts=logstash
ENV LS_JAVA_OPTS="-Xms512m -Xmx512m"

WORKDIR /logstash

COPY nginx.log ./
COPY /pipeline ./pipeline

EXPOSE 5000
EXPOSE 5044
EXPOSE 9600

CMD [ "logstash", "-f", "pipeline/logstash-nginx.config" ]