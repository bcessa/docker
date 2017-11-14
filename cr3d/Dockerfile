# Cr3dOv3r
# Credential reuse scanner
# https://github.com/D4Vinci/Cr3dOv3r
# docker build -t cr3d .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y git-core python3-pip

RUN \
  cd /opt && \
  git clone https://github.com/D4Vinci/Cr3dOv3r.git && \
  cd Cr3dOv3r && \
  pip3 install -r requirements.txt

ENTRYPOINT ["/usr/bin/python3", "/opt/Cr3dOv3r/Cr3dOv3r.py"]
