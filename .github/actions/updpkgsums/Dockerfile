FROM docker.io/library/archlinux:base-devel@sha256:6db772fd1dd128b9cf7b7231ca5284af70879596fe4ec754c911cfc4ac30d5eb

RUN pacman -Syu --needed --noconfirm pacman-contrib namcap git sudo && \
  useradd -m builder && \
  echo 'builder ALL=(ALL) NOPASSWD: ALL' >> /etc/sudoers

WORKDIR /home/builder
USER builder

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT [ "/entrypoint.sh" ]
