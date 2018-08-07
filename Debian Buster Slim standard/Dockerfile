FROM fernandoenzo/debian:10s-min
MAINTAINER Fernando Enzo Guarini (fernandoenzo@gmail.com)

COPY scripts/basics /tmp
RUN bash /tmp/basics

ENTRYPOINT service cron start > /dev/null 2>&1 ; dpkg-reconfigure openssh-server > /dev/null 2>&1 ; /bin/bash
