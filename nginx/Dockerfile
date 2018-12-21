FROM nginx:alpine

LABEL maintainer="Mahmoud Zalt <mahmoud@zalt.me>"

COPY nginx.conf /etc/nginx/

RUN apk update \
    && apk upgrade \
    && apk add --no-cache openssl \
    && apk add --no-cache bash \
    && adduser -D -H -u 1000 -s /bin/bash www-data \
    && mkdir /var/www/ \
    && mkdir /var/www/html

# Set upstream conf and remove the default conf
RUN rm /etc/nginx/conf.d/default.conf

COPY sites/*.conf /etc/nginx/conf.d/

ADD ./startup.sh /opt/startup.sh
CMD ["/bin/bash", "/opt/startup.sh"]

EXPOSE 80 443
