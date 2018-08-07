FROM debian:buster-slim
MAINTAINER Fernando Enzo Guarini (fernandoenzo@gmail.com)

COPY scripts/basics /tmp
COPY scripts/install-language /tmp
COPY static/systemd /etc/apt/preferences.d/
COPY static/bashrc /root/.bashrc
COPY static/bashrc /etc/skel/.bashrc
COPY static/bash_aliases /root/.bash_aliases
COPY static/bash_aliases /etc/skel/.bash_aliases
COPY static/tmux.conf /root/.tmux.conf
COPY static/tmux.conf /etc/skel/.tmux.conf
COPY static/tmux.conf.local /root/.tmux.conf.local
COPY static/tmux.conf.local /etc/skel/.tmux.conf.local
COPY ["static/Apuntes tmux.txt", "/root"]
COPY ["static/Apuntes tmux.txt", "/etc/skel"]

RUN apt-get update ; apt-get install -y --no-install-recommends aptitude
RUN bash /tmp/install-language
RUN bash /tmp/basics

ENV LANG es_ES.UTF-8
ENV TERM xterm-256color

ENTRYPOINT service cron start > /dev/null 2>&1 ; /bin/bash
