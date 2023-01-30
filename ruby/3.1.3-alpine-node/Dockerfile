FROM amd64/ruby:3.1.3-alpine

RUN apk -v --update add \
      build-base \
      bash \
      ruby-dev \
      imagemagick-dev \
      imagemagick \
      libxml2 \
      libxml2-dev \
      nodejs \
      zlib-dev \
      postgresql-dev \
      tzdata \
      git \
    && rm /var/cache/apk/*
