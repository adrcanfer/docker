FROM nginx:latest

RUN apt-get update;
RUN apt-get install -y vim;

COPY ./static /usr/share/nginx/html
VOLUME "nginx-vol:/usr/share/nginx/html"