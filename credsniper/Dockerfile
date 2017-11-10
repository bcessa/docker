# CredSniper
# Phishing framework which supports capturing 2FA tokens
# https://github.com/ustayready/CredSniper
# docker build -t credsniper .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y git-core python3-pip

RUN \
  cd /opt && \
  git clone https://github.com/ustayready/CredSniper && \
  cd CredSniper && \
  pip3 install -r requirements.txt

ENTRYPOINT ["/usr/bin/python3", "/opt/CredSniper/credsniper.py"]
