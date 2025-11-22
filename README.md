# bootc Packages for Arch Linux

This repository includes a few packages that are useful to boot [Arch Linux](https://archlinux.org) while utilizing [bootc](https://github.com/bootc-dev/bootc). All packages are listed in the `pkgs/` folder in the repository root.

## Using the repository

In order to install packages from this repository via `pacman`, you need to import the signing key:

```bash
pacman-key --init
pacman-key --recv-key 5DE6BF3EBC86402E7A5C5D241FA48C960F9604CB --keyserver keyserver.ubuntu.com
pacman-key --lsign-key 5DE6BF3EBC86402E7A5C5D241FA48C960F9604CB
```

And add the following to `/etc/pacman.conf`:
```ini
[archzfs]
SigLevel = Required
Server = https://github.com/archzfs/archzfs/releases/download/experimental
```

Afterwards, sync your repositories with `pacman -Sy`, and then install a package like so:

```bash
pacman -S bootc
```
