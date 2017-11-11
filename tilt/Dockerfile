# Tilt
# An automatic ip lookup and reverse probing tool for passive reconnaissance
# https://github.com/AeonDave/tilt
# docker build -t tilt .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y git-core python-pip

RUN \
  cd /opt && \
  git clone https://github.com/AeonDave/tilt.git && \
  cd tilt && \
  pip install beautifulsoup4

ENTRYPOINT ["/usr/bin/python", "/opt/tilt/tilt.py"]
