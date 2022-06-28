FROM node:16.14.0 as build-step
RUN mkdir -p /app
WORKDIR /app
COPY . /app
FROM nginx:1.17.1
COPY --from=build-step /app/dist/liquidando /usr/share/nginx/html
