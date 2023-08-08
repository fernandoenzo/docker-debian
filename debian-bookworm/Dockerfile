FROM debian:bookworm-slim as debian

COPY contents/ /tmp/contents

RUN bash /tmp/contents/scripts/basics


FROM scratch
COPY --from=debian / /

ENV LANG es_ES.UTF-8
ENV TERM xterm-256color

ENTRYPOINT ["/usr/local/boot"]
CMD ["/bin/bash"]
