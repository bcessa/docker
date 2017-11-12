# OnionShare
# Securely and anonymously share a file
# https://github.com/micahflee/onionshare
# docker build -t onionshare .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y \
    build-essential \
    dh-python \
    fakeroot \
    git-core \
    python3-all \
    python3-stdeb \
    python3-flask \
    python3-stem \
    python3-pyqt5 \
    python-nautilus \
    python3-pytest \
    tor

RUN \
  cd /opt && \
  git clone https://github.com/micahflee/onionshare.git

WORKDIR /opt/onionshare/

ENTRYPOINT ["./dev_scripts/onionshare"]
