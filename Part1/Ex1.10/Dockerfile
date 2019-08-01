# https://github.com/docker-hy/frontend-example-docker

FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl python-software-properties
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs

RUN node -v && npm -v

COPY . .
EXPOSE 5000
RUN npm install
RUN npm install -g serve
RUN npm run build
CMD ["serve", "-s", "-l", "5000", "dist"]
