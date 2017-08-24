# Portia - Penetration test tool
# https://github.com/SpiderLabs/portia
# docker build -t portia .
FROM ubuntu:16.04

# Base
RUN \
  apt update && \
  apt install -y autoconf automake autopoint libtool pkg-config freetds-dev python-pip git-core && \
  pip install pysmb tabulate termcolor xmltodict pyasn1 pycrypto pyOpenSSL dnspython netaddr python-nmap

# impacket
RUN \
  cd /opt && \
  git clone https://github.com/CoreSecurity/impacket && \
  cd impacket && \
  python setup.py install

# libesedb
RUN \
  cd /opt && \
  git clone https://github.com/libyal/libesedb.git && \
  cd libesedb && \
  ./synclibs.sh && \
  ./autogen.sh

# ntdsxtract
RUN \
  cd /opt && \
  git clone https://github.com/csababarta/ntdsxtract && \
  cd ntdsxtract && \
  python setup.py install && \
  pip install git+https://github.com/pymssql/pymssql.git

# volatility
RUN \
  cd /opt && \
  git clone https://github.com/volatilityfoundation/volatility && \
  cd volatility && \
  python setup.py install

RUN \
  cd /opt && \
  git clone https://github.com/SpiderLabs/portia

RUN apt clean && apt autoremove -y

ENTRYPOINT ["/opt/portia/portia.py"]
