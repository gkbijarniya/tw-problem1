# alpine 3.3/NGINX
FROM nginx:1.9.15-alpine

RUN apk --update add unzip
    
ADD https://s3.amazonaws.com/infra-assessment/static.zip /tmp/
RUN unzip -d /usr/share/nginx/html/ /tmp/static.zip && rm -f /tmp/static.zip

COPY default.conf /etc/nginx/conf.d/default.conf
