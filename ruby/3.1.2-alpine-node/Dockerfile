FROM amd64/ruby:3.1.2-alpine

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
