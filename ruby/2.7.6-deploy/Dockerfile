ARG BASE_IMAGE=amd64/ruby
ARG BASE_TAG=2.7.6
ARG BASE_IMAGE=${BASE_IMAGE}:${BASE_TAG}

FROM ${BASE_IMAGE}

RUN apt-get update -qq \
  && apt-get install -y \
  build-essential \
  ca-certificates \
  imagemagick \
  libpq-dev \
  python2 \
  shared-mime-info \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*
