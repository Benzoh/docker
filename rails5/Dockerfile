# Docker for Mac がずいぶん良いらしいので、Docker で Rails アプリを動かしてみた - えいのうにっき
# http://blog.a-know.me/entry/2016/06/29/165652

# Quickstart: Compose and Rails | Docker Documentation
# https://docs.docker.com/compose/rails/#build-the-project

# Best practices for writing Dockerfiles | Docker Documentation
# https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

FROM ruby:2.3.3
ENV LANG C.UTF-8
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs npm nodejs-legacy
# RUN npm install -g phantomjs-prebuilt
RUN gem install bundler

ENV APP_HOME /sample_app_home
RUN mkdir $APP_HOME
WORKDIR $APP_HOME
COPY Gemfile /sample_app_home/Gemfile
COPY Gemfile.lock /sample_app_home/Gemfile.lock
# ADD Gemfile* $APP_HOME/

RUN bundle install

COPY . /sample_app_home
# ADD . $APP_HOME