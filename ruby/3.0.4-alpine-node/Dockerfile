FROM amd64/ruby:3.0.4-alpine

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
