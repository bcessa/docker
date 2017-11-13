# Enigma
# Multiplatform payload dropper
# https://github.com/UndeadSec/Enigma
# docker build -t enigma .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y git-core python-pip

RUN \
  cd /opt && \
  git clone https://github.com/UndeadSec/Enigma.git

ENTRYPOINT ["/usr/bin/python", "/opt/Enigma/enigma.py"]
