# chroot-distro
Perintah membuat Rootfs Debian untuk Termux:
```
sudo apt update && sudo apt upgrade
sudo apt install debootstrap qemu-user-static
sudo debootstrap --arch=arm64 trixie ./debian-arm64 http://deb.debian.org/debian
cd debian-arm64
sudo tar --numeric-owner -czf ../debian-13-trixie-arm64-rootfs.tar.gz .
```
