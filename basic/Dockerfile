FROM debian:stable-slim

RUN echo 'Hola Mundo desde RUN'

ARG arg1
RUN echo ${arg1}

RUN apt-get update;
RUN apt-get install -y vim;

ENV env1="Hola Mundo desde ENV"

COPY file.txt tmp/file.txt
CMD [ "sleep", "3600" ]

