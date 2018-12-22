ARG ELK_VERSION

FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

#COPY ./config/elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml
#COPY ./plugins/ik /usr/share/elasticsearch/plugins/ik

RUN yum install -y unzip \
    && cd ~ \
    && mkdir ik \
    && cd ik \
    && wget https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v6.4.2/elasticsearch-analysis-ik-6.4.2.zip \
    && unzip elasticsearch-analysis-ik-6.4.2.zip \
    && mkdir /usr/share/elasticsearch/plugins/ik \
    && cp -R * /usr/share/elasticsearch/plugins/ik/

# RUN elasticsearch-plugin install analysis-kuromoji
# RUN elasticsearch-plugin remove x-pack

EXPOSE 9200 9300
