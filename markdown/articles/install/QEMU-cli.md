---
title: Running dahliaOS in QEMU (cli)
permalink: install/QEMU-cli.html
summary: How to run dahliaOS Linux inside of the QEMU Emulator
---
## dahliaOS on QEMU

### Linux

#### Arch
- First open a terminal and type the following command:

```
sudo pacman -S qemu qemu-arch-extra qemu-block-gluster qemu-block-iscsi qemu-block-rbd samba
```

#### Fedora 32 - 36
- First open a terminal and type the following command:

```
sudo dnf install qemu
```

#### Gentoo
- First open a terminal and type the following command:

```
emerge --ask app-emulation/qemu
```

#### Ubuntu 20.04 - 22.04
- First open a terminal and type the following command:

```
sudo apt install qemu-kvm qemu virt-manager virt-viewer libvirt-daemon-system libvirt-clients
```

- For **Ubuntu 18.04** or older you want to run this command: 

```
sudo apt-get install qemu-kvm qemu virt-manager virt-viewer libvirt-bin
```

### Run dahliaOS
- Download the dahliaOS latest ISO from: https://github.com/dahliaos/releases/releases/latest

- Then type the following command in the terminal (make sure that you use the right name of the ISO file. DahliaOS.iso is just for this example)

- Make sure you use a least 2GB or more or the vm will fail to load pangolin

```
qemu-system-x86_64 -cdrom Downloads/DahliaOS.iso -m 2048 -enable-kvm
```
