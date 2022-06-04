#Stage 1: Build an angular docker image
FROM node:10.16.0-alpine as build
LABEL Maintainer="lmoyano"
WORKDIR /app
COPY package*.json /app/
RUN npm install && npm cache clean --force
COPY . /app
ARG CONFIGURATION=production
RUN npm run build -- --outputPath=./dist/woff --configuration $CONFIGURATION

#Stage2, use the compiled app, ready for production
FROM nginx:1.22.0-alpine
COPY --from=build /app/dist/woff/ /usr/share/nginx/html