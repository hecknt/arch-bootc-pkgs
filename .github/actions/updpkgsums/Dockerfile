FROM docker.io/library/archlinux:base-devel@sha256:70d777aaeb45befc04150df137c4d7c1b5042be442b4c904c38c6f6880bb7844

RUN pacman -Syu --needed --noconfirm pacman-contrib namcap git sudo && \
  useradd -m builder && \
  echo 'builder ALL=(ALL) NOPASSWD: ALL' >> /etc/sudoers

WORKDIR /home/builder
USER builder

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT [ "/entrypoint.sh" ]
