# FatCat
# FAT filesystems explore, extract, repair, and forensic tool
# https://github.com/Gregwar/fatcat
# docker build -t fatcat .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y git-core build-essential cmake

RUN \
  cd /opt && \
  git clone https://github.com/Gregwar/fatcat.git && \
  cd fatcat && \
  mkdir build && \
  cd build && \
  cmake .. && \
  make && \
  mv fatcat /usr/local/bin/.

RUN \
  apt install -y git-core build-essential cmake && \
  apt autoremove -y && \
  apt clean && \
  rm -rf /opt/fatcat

ENTRYPOINT ["/usr/local/bin/fatcat"]
