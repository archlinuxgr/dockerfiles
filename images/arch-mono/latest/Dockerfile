FROM nfnty/arch-mini:latest
MAINTAINER nfnty <docker@nfnty.se>

ENV VERSION_MONO='4.8.0.495-1'
RUN pacman --sync --noconfirm --refresh --sysupgrade && \
    pacman --sync --noconfirm "mono=${VERSION_MONO}" && \
    find /var/cache/pacman/pkg -mindepth 1 -delete
