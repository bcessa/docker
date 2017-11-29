# XSS Sniper - An automatic XSS discovery tool
# https://github.com/gbrindisi/xsssniper
# docker build -t xsssniper .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y python-pip git-core && \
  cd /opt && \
  git clone https://github.com/gbrindisi/xsssniper && \
  pip install mechanize lxml

RUN \
  apt purge -y git-core && \
  apt autoremove -y

ENTRYPOINT ["/usr/bin/python", "/opt/xsssniper/xsssniper.py"]
