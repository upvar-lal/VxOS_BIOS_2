# VxOS

VxOS is a Debian Live-based Linux desktop image for x86_64 virtual machines.

## Included components

- Debian Stable base with Linux kernel
- XFCE desktop and LightDM
- NetworkManager for network configuration
- Debian firmware packages for supported hardware
- Chromium browser
- Google Chrome stable package when the official download is available during the build

## Build

1. Open the **Actions** tab in this repository.
2. Select **Build VxOS**.
3. Press **Run workflow** on the `main` branch.
4. Wait for the build to finish.
5. Open the completed workflow run and download the `VxOS-amd64-images` artifact.

The artifact contains:
- `VxOS-amd64.iso`: bootable hybrid ISO for a virtual machine.
- `VxOS-amd64.img`: the same hybrid image with an IMG filename.
- `SHA256SUMS.txt`: checksums for verifying both files.

## Notes

The ISO/IMG is intended for x86_64 (AMD64) virtual machines. In a VM, networking is normally presented as a virtual Ethernet adapter; Wi-Fi firmware only helps when compatible physical or virtual hardware is exposed to Linux. Hardware support depends on the device and firmware availability.

This repository builds the image in GitHub Actions; no local computer is required to run the build.
