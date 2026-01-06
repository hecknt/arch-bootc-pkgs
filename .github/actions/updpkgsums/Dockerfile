FROM docker.io/library/archlinux:base-devel@sha256:ebcaeca69c4d416f848aedcd27fe224384fd506f86046526a5d49ec6d9e29db1

RUN pacman -Syu --needed --noconfirm pacman-contrib namcap git sudo && \
  useradd -m builder && \
  echo 'builder ALL=(ALL) NOPASSWD: ALL' >> /etc/sudoers

WORKDIR /home/builder
USER builder

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT [ "/entrypoint.sh" ]
