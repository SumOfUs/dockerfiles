FROM ruby:2.4.5-stretch
RUN curl -sL https://deb.nodesource.com/setup_11.x | bash - \
  && curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
  && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list \
  && apt-get update \
  && apt-get install -y gettext-base python python-pip libpython-dev nodejs yarn -qq
RUN pip install awscli --upgrade --user
RUN gem install bundler
ENV PATH "$PATH:~/.local/bin"

