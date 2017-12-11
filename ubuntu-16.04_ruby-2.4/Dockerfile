FROM ubuntu:16.04

# basic utils
RUN apt-get update && apt-get install -y apt-utils gcc build-essential zlib1g-dev libssl-dev

# ruby
WORKDIR /tmp
RUN apt-get install -y wget \
      && wget -q https://cache.ruby-lang.org/pub/ruby/2.4/ruby-2.4.2.tar.gz -O ruby-2.4.2.tar.gz \
      && tar -xf ruby-2.4.2.tar.gz \
      && cd ruby-2.4.2 \
      && ./configure \
      && make \
      && make install

RUN gem install bundler -v 1.14.6
