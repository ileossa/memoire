#get base image ubuntu 16.10
FROM ubuntu:yakkety


ENV WEAVE_MEMOIRE nointeractive

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

# Get package and install
RUN \
  apt-get update && \
  apt-get -y install \
      git-core \
      ssh \
      build-essential \
      g++ \
      doxygen \
      libcurl4-openssl-dev \
      libgoogle-perftools-dev \
      python-jinja2 \
      autoconf \
      automake \
      binutils \
      cmake \
      hostapd \
      libavahi-client-dev \
      libtool \
      libssl-dev \
      libevent-dev \
      libexpat1-dev



# Download and build Weave and run test integration
RUN git clone https://weave.googlesource.com/weave/libiota \
    cd libiota \
    make -j lib \
    make test \
