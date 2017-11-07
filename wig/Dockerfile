# wig - WebApp Information Gatherer
# https://github.com/jekyc/wig
# docker build -t wig .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y python3 git-core && \
  cd /opt && \
  git clone https://github.com/jekyc/wig

ENTRYPOINT ["/usr/bin/python3", "/opt/wig/wig.py"]
