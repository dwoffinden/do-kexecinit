# init replacement bootstrap for Arch Linux on Digital Ocean / KVM

This package replaces the init script with a script that uses kexec to boot the stock Arch Linux kernel.

This allows running the stock Arch Linux kernel on KVM providers like Digital Ocean.

## Directions

Build and install the package, reboot your vps/droplet. This package will install kexec-tools and the kernel from Arch Linux repositories. It will also remove systemd-sysvcompat.

## Warning

Usage of this is not currently supported by Digital Ocean and at any time they could make a change to their system that would be incompatible and render your VPS unbootable. 

## License 

This script is distributed under the MIT License (see LICENSE)
