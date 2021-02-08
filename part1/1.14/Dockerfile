FROM ruby:2.6.0

WORKDIR /app

RUN gem install bundler

RUN apt-get update && apt-get install git && apt-get install -y nodejs

RUN git clone https://github.com/docker-hy/rails-example-project.git

WORKDIR /app/rails-example-project

RUN bundle install

RUN rails db:migrate

EXPOSE 3000

CMD [ "rails", "s" ]
