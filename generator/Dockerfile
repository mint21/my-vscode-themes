# This is an updated Dockerfile from https://github.com/microsoft/vscode-generator-code
# A newer node base image is used
FROM node:alpine3.22

RUN apk update && apk add git

RUN npm install -g yo generator-code
RUN chown -R node:node /usr/local/lib/node_modules

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install

COPY . .

RUN chown -R node:node /usr/src/app
USER node
ENTRYPOINT [ "yo", "code" ]
