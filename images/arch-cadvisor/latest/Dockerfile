FROM nfnty/arch-mini:latest
MAINTAINER nfnty <docker@nfnty.se>

ENV VERSION_CADVISOR='0.25.0-1'
RUN pacman --sync --noconfirm --refresh --sysupgrade && \
    pacman --sync --noconfirm "nfnty/cadvisor=${VERSION_CADVISOR}" && \
    find /var/cache/pacman/pkg -mindepth 1 -delete

USER root
EXPOSE 8080/tcp
ENTRYPOINT ["/usr/bin/cadvisor"]
