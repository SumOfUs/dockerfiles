FROM amd64/ruby:2.7.6-alpine

RUN apk -v --update add \
      build-base \
      bash \
      ruby-dev \
      imagemagick6-dev \
      imagemagick6 \
      nodejs \
      zlib-dev \
      postgresql-dev \ 
      tzdata \
      git \
    && rm /var/cache/apk/*
