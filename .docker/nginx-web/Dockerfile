FROM nginx:1.17
RUN apt-get update && apt-get install curl -y
RUN curl -L -O https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-7.8.1-amd64.deb && \
    dpkg -i filebeat-7.8.1-amd64.deb
RUN mkdir -p /var/www
ADD nginx-config/default.conf /etc/nginx/conf.d/default.conf
ADD nginx-config/index.html /var/www/index.html
ADD nginx-config/nginx.conf /etc/nginx/nginx.conf
