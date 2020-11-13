FROM alpine:3.12

RUN set -x && \
    apk add --no-cache rsync tini && \
    mkdir -p /var/krill/data/repo

COPY rsyncd.conf /etc/

VOLUME /var/krill/data/repo
EXPOSE 873/tcp

ENTRYPOINT ["/sbin/tini", "--", "rsync"]
CMD ["--daemon", "--no-detach", "--log-file=/dev/stdout"]
