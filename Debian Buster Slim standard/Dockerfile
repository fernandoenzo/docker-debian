FROM fernandoenzo/debian:10s-min
MAINTAINER Fernando Enzo Guarini (fernandoenzo@gmail.com)

COPY scripts/basics /tmp
RUN bash /tmp/basics

ENTRYPOINT dpkg-reconfigure openssh-server > /dev/null 2>&1 ; /bin/bash
