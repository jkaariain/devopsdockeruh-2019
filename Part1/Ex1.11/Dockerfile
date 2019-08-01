# https://github.com/docker-hy/backend-example-docker

FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl python-software-properties
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs

RUN node -v && npm -v

COPY . .
EXPOSE 8000
RUN npm install
CMD ["npm", "start"]

