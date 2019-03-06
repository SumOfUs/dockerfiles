FROM ruby:2.6.1-alpine as ruby

RUN gem install bundler
RUN bundle config --global silence_root_warning 1

RUN apk -v --update add \
      python \
      py-pip \
      groff \
      less \
      mailcap \
      bash \
      nodejs \
      yarn \
      tzdata \
      git \
    && pip install --upgrade awscli==1.14.5 s3cmd==2.0.1 python-magic \
    && apk -v --purge del py-pip \
    && apk add flow --update-cache --repository http://dl.alpinelinux.org/alpine/edge/testing/ \
    && apk add build-base \
      ruby-dev \
      imagemagick6-dev \
      imagemagick6 \
      zlib-dev \
      postgresql-dev \ 
    && rm /var/cache/apk/*

ENV PATH "$PATH:~/.local/bin"

