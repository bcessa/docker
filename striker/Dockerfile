# Striker - Offensive information and vulnerability scanner
# https://github.com/UltimateHackers/Striker
# docker build -t striker .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y python-pip git-core && \
  cd /opt && \
  git clone https://github.com/UltimateHackers/Striker.git && \
  cd Striker && \
  pip install --upgrade pip && \
  pip install -r requirements.txt

ENTRYPOINT ["/usr/bin/python", "/opt/Striker/striker.py"]
