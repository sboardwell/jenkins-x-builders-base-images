ARG FROM_IMAGE=to-be-set-in-the-skaffold-yaml
ARG FROM_VERSION=to-be-set-in-the-skaffold-yaml
FROM $FROM_IMAGE:$FROM_VERSION

RUN yum install -y gcc \
    && yum clean all 

RUN wget -q https://static.rust-lang.org/rustup/dist/x86_64-unknown-linux-gnu/rustup-init && \
  chmod +x rustup-init &&\
  ./rustup-init -y &&\
  rm -rf rustup-init

ENV PATH=$PATH:/root/.cargo/bin
RUN rustup override set nightly
