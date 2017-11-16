# ROCA
# RSA vulnerability scanner
# https://crocs.fi.muni.cz/public/papers/rsa_ccs17
# docker build -t roca .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y python-pip python-dev build-essential libssl-dev libffi-dev swig && \
  pip install roca-detect

ENTRYPOINT ["/usr/local/bin/roca-detect"]
