FROM docker.io/library/archlinux:base-devel@sha256:624bdc7fc6615155d67bc34cf7146c0c9fd0e3c92943977da63a630e4ca49c30

RUN pacman -Syu --needed --noconfirm pacman-contrib namcap git sudo && \
  useradd -m builder && \
  echo 'builder ALL=(ALL) NOPASSWD: ALL' >> /etc/sudoers

WORKDIR /home/builder
USER builder

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT [ "/entrypoint.sh" ]
