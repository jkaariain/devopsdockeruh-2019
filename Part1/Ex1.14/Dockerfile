# https://github.com/docker-hy/rails-example-project

FROM ruby:2.6.0

WORKDIR /app
COPY . .
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_12.x | bash -
RUN apt-get install -y nodejs
RUN npm install yarn -g

RUN bundle install
RUN rails db:migrate
RUN rake assets:precompile

EXPOSE 3000
CMD ["rails", "s"]
