FROM cimg/ruby:2.7.6-browsers

# Add repository sources & transports
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - \
  && echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list \
  && sudo apt-get install apt-transport-https \
  && sudo apt-get update

# Add packages:
RUN sudo apt-get install yarn python3-pip gettext-base \
  && pip3 install awscli --upgrade --user

# Set path for awscli
ENV PATH "$PATH:~/.local/bin"

# Update bundler
RUN gem install bundler:2.3.15
