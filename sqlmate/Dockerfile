# sqlmate
# Tool which will do what you always expected from SQLmap
# https://github.com/UltimateHackers/sqlmate
# docker build -t sqlmate .
FROM ubuntu:16.04

RUN \
  apt update && \
  apt install -y python-pip git-core && \
  cd /opt

RUN \
  git clone https://github.com/UltimateHackers/sqlmate && \
  cd /opt/sqlmate && \
  pip install \
    mechanize \
    bs4 \
    HTMLparser \
    argparse \
    requests \
    urlparse2

COPY start.sh /start.sh

RUN \
  apt remove -y git-core && \
  apt clean && \
  apt autoremove -y && \
  chmod 775 /start.sh

ENTRYPOINT ["/start.sh"]
