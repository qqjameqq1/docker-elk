ARG ELK_VERSION

FROM docker.elastic.co/kibana/kibana:${ELK_VERSION}

COPY ./config/kibana.yml /opt/kibana/config/kibana.yml
# RUN kibana-plugin remove x-pack

EXPOSE 5601
