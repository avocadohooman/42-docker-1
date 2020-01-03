FROM ruby:latest

LABEL maintainer="gmolin@student.hive.fi"

RUN apt-get update -y && \
	apt-get install -y 	nodejs && \
	apt-get install -y  build-essential && \
	apt-get install -y  libpq-dev && \
	apt-get install -y  sqlite3

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000

ONBUILD RUN bundle update
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed
