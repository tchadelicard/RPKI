FROM nginx:stable-alpine

RUN rm /etc/nginx/conf.d/default.conf
COPY rrdp.conf /etc/nginx/rrdp.conf

RUN mkdir -p /var/krill/data/repo
VOLUME /var/krill/data/repo

EXPOSE 3000/tcp
