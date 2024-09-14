FROM ubuntu/postgres:14-22.04_beta as ubuntu

ENV working_dir ""
ENV HOSTNAME=localhost

WORKDIR $working_dir

SHELL ["/bin/bash", "--login", "-c"]
RUN apt-get update && \
apt-get install -y apt-transport-https \
  software-properties-common \
  wget \
  libssl-dev \
  openssl \
  build-essential zlib1g-dev \
  curl \
  git &&\
  apt -y autoremove && \
  apt-get clean && \
  mkdir -p /caritas/data

#CMD ["sleep", "infinity"]