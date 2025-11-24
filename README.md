# bootc Packages for Arch Linux

This branch of this repository includes a few packages that are actively being tested. It is not advised to use this repository for day-to-day usage.

## Using the repository

In order to install packages from this repository via `pacman`, you need to import the signing key:

```bash
pacman-key --init
pacman-key --recv-key 5DE6BF3EBC86402E7A5C5D241FA48C960F9604CB --keyserver keyserver.ubuntu.com
pacman-key --lsign-key 5DE6BF3EBC86402E7A5C5D241FA48C960F9604CB
```

And add the following to `/etc/pacman.conf`:
```ini
[bootc-testing]
SigLevel = Required
Server = https://github.com/hecknt/arch-bootc-pkgs/releases/download/$repo
```

Afterwards, sync your repositories with `pacman -Sy`, and then install a package like so:

```bash
pacman -S bootc-git
```
