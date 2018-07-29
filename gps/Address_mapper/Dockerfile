FROM ruby:2.5.1
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
RUN mkdir /proyecto1docker
WORKDIR /proyecto1docker
COPY Gemfile .
COPY Gemfile.lock .
RUN bundle install
COPY . .
RUN ls .
RUN rake db:migrate
EXPOSE 3000
CMD rails