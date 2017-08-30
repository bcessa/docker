# SQLMap
# Automatic SQL Injection And Database Takeover Tool
# https://github.com/sqlmapproject/sqlmap
# docker build -t sqlmap .
FROM alpine:3.6

RUN \
  apk add --update python git && \
  rm -rf /var/cache/apk/*

RUN \
  git clone --depth 1 https://github.com/sqlmapproject/sqlmap.git sqlmap-dev

ENTRYPOINT ["python", "/sqlmap-dev/sqlmap.py"]
