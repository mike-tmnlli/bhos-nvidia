# BlueHatOS (NVIDIA) &nbsp; [![bluebuild build badge](https://github.com/mike-tmnlli/bhos-nvidia/actions/workflows/build.yml/badge.svg)](https://github.com/mike-tmnlli/bhos-nvidia/actions/workflows/build.yml)

## Installation

To rebase an existing atomic Fedora installation to the latest build:

- First rebase to the unsigned image, to get the proper signing keys and policies installed:
  ```
  rpm-ostree rebase ostree-unverified-registry:ghcr.io/mike-tmnlli/bhos-nvidia:latest
  ```
- Reboot to complete the rebase:
  ```
  systemctl reboot
  ```
- Then rebase to the signed image, like so:
  ```
  rpm-ostree rebase ostree-image-signed:docker://ghcr.io/mike-tmnlli/bhos-nvidia:latest
  ```
- Reboot again to complete the installation
  ```
  systemctl reboot
  ```
