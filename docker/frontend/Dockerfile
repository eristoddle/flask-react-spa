FROM node:8.6-alpine

RUN apk add --no-cache git

COPY ./package.json /flask/package.json

WORKDIR /flask

RUN npm install

COPY ./frontend /flask/frontend

RUN npm run build:dll

COPY ./docker/frontend/frontend-entrypoint.sh /
