# Base ruby
FROM ruby:2.6.1-alpine as ruby

# Base node + yarn
FROM node:11-alpine as node

# aws-cli
RUN apk -v --update add \
      python \
      py-pip \
      groff \
      less \
      mailcap \
      && \
    pip install --upgrade awscli==1.14.5 s3cmd==2.0.1 python-magic && \
    apk -v --purge del py-pip && \
    rm /var/cache/apk/*

RUN gem install bundler

ENV PATH "$PATH:~/.local/bin"

