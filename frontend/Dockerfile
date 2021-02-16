# build stage
FROM node:12-alpine
WORKDIR /frontend

COPY ./package-lock.json ./package.json ./
RUN npm ci
COPY . .