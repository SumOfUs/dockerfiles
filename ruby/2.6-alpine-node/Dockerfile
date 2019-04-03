FROM ruby:2.6-alpine

RUN gem install bundler:2.0.1
RUN bundle config --global silence_root_warning 1

RUN apk -v --update add \
      build-base \
      bash \
      ruby-dev \
      imagemagick6-dev \
      imagemagick6 \
      zlib-dev \
      postgresql-dev \ 
      nodejs \
      yarn \
      tzdata \
      git \
    && rm /var/cache/apk/*

