# CI and Testing

Following Tests are done on Travis-CI.

- `shellcheck` every executable script (Job #build.1)
- Test on Artful container (Job #build.2)
- Test on Xenial container (Job #build.3)
- Test on Trusty (Host) (Job #build.4) (Soon to be removed)
- Test on Bionic Beaver (Job #build.5)

!!! info
    Trusty tests do not install indicator-kdeconnect, peek, openjdk-8-jdk, gnome-todo , gnome-calendar, polari and their PPAs. Please modify your lists accordingly.

- Test on Cosmic Cuttlefish (Job #build.6) using base image from `http://cdimage.ubuntu.com/ubuntu-base/daily/`
- Build documentation using mkdocs (Job #build.7).
- Dockerfiles used for building the image are in `/dockerfiles` directory, they use official Ubuntu base images with script dependencies.
- Test scripts are located in `/tests` directory.
- Since its a time consuming process only simulated install is done on CI. Linux mint and Elementary are not tested in containers as of now, but will be in the future.
- It is possible that there might be some errors specific to your setup. Please report if so. It is **Strongly** advised to try install apps and deb files in simulate mode first before proceeding with actual installation.

!!! warning
    Never set environment variable `TRAVIS=true` unless you are running on TRAVIS or are sure of its effects.