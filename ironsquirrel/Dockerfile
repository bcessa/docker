# IronSquirrel
# Encrypted browser exploit delivery
# https://github.com/MRGEffitas/Ironsquirrel
# docker build -t ironsquirrel .
FROM ubuntu:16.04

# Deps
RUN \
  apt update && \
  apt install -y git-core ruby-dev build-essential libz-dev && \
  gem install bundler

# Clone repo
RUN \
  git clone https://github.com/MRGEffitas/Ironsquirrel.git && \
  cd Ironsquirrel && \
  bundle config --global silence_root_warning 1 && \
  bundle install

# Cleanup
RUN \
  apt remove -y git-core build-essential && \
  apt clean && \
  apt autoremove -y

# Executable
WORKDIR /Ironsquirrel
ENTRYPOINT ["/usr/bin/ruby", "IRONSQUIRREL.rb"]
