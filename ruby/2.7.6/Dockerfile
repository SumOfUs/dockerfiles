ARG BASE_IMAGE=amd64/ruby
ARG BASE_TAG=2.7.6
ARG BASE_IMAGE=${BASE_IMAGE}:${BASE_TAG}

FROM ${BASE_IMAGE}

RUN apt-get update -qq \
  && apt-get install -y \
  build-essential \
  ca-certificates \
  curl \
  gettext-base \
  git \
  gnupg \
  imagemagick \
  jest \
  jq \
  libpq-dev \
  lsb-release \
  python2 \
  python3-pip \
  shared-mime-info \
  zip \
  && mkdir -p /etc/apt/keyrings \
  && curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /etc/apt/keyrings/docker.gpg \
  && echo \
  "deb [arch=$(dpkg --print-architecture) \
  signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null \
  && curl -sL https://deb.nodesource.com/setup_14.x | bash \
  && curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
  && echo "deb https://dl.yarnpkg.com/debian/ stable main" \
  > /etc/apt/sources.list.d/yarn.list \
  && apt-get update -qq \
  && apt-get install -y \
  docker-ce \
  docker-ce-cli \
  containerd.io \
  nodejs \
  yarn \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* \
  && pip3 install awscli --upgrade --user

# Set path for awscli
ENV PATH "$PATH:~/.local/bin"

RUN gem install bundler:2.3.24

ARG RAILS_ROOT=/app/
WORKDIR $RAILS_ROOT

COPY . .
