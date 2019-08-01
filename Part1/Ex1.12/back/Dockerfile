# https://github.com/docker-hy/backend-example-docker

FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl python-software-properties
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs

RUN node -v && npm -v

COPY . .
EXPOSE 8000
RUN npm install

# This is the guest OS IP address, since I'm working with Docker inside a Linux VM (Without GUI).
# Replace with http://localhost:1234 when not using a VM.
ENV FRONT_URL=http://192.168.56.5:1234
CMD ["npm", "start"]

