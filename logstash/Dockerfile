ARG ELK_VERSION

FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}

#ADD ./config/logstash.conf /usr/share/logstash/pipeline/logstash.conf
ADD ./config/filebeat.conf /usr/share/logstash/pipeline/filebeat.conf

#COPY ./config/logstash.yml /opt/logstash/config/logstash.yml

EXPOSE 5044
