# SQLiv
# Massive SQL Injection Vulnerability Scanner
# https://github.com/Hadesy2k/sqliv
# docker build -t sqliv .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y python-pip git-core && \
  cd /opt

RUN \
  git clone https://github.com/Hadesy2k/sqliv.git && \
  cd /opt/sqliv && \
  python2 setup.py -i

COPY start.sh /start.sh

RUN \
  apt remove -y git-core && \
  apt clean && \
  apt autoremove -y && \
  chmod 775 /start.sh

ENTRYPOINT ["/start.sh"]
