FROM docker.io/library/archlinux:base-devel@sha256:f6b259c6c0cd1bc4c86510485acb6a5f053c15789c9c68c7434b6fe99564906c

RUN pacman -Syu --needed --noconfirm pacman-contrib namcap git sudo && \
  useradd -m builder && \
  echo 'builder ALL=(ALL) NOPASSWD: ALL' >> /etc/sudoers

WORKDIR /home/builder
USER builder

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT [ "/entrypoint.sh" ]
