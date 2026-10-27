![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/gaofengnan/starship-debian/total)
![GitHub Downloads (all assets, latest release)](https://img.shields.io/github/downloads/gaofengnan/starship-debian/latest/total)
![GitHub Release](https://img.shields.io/github/v/release/gaofengnan/starship-debian)
![GitHub Release Date](https://img.shields.io/github/release-date/gaofengnan/starship-debian?display_date=published_at)

# starship for Debian

> Fork of [dariogriffo/starship-debian](https://github.com/dariogriffo/starship-debian) (MIT); the original packaging is by Dario Griffo. Served at [deb.gaofn.xyz](https://deb.gaofn.xyz) for Debian 12 (bookworm) and 13 (trixie).

This repository contains build scripts to produce the _unofficial_ Debian packages
(.deb) for [starship](https://github.com/starship/starship) hosted at [deb.gaofn.xyz](https://deb.gaofn.xyz)

Currently supported Debian distros are:
- Bookworm (v12)
- Trixie (v13)
- Forky (v14)
- Sid (testing)

**Upstream architectures:** amd64, arm64, armhf, i386 and riscv64. No ppc64el, s390x or armel.

This is an unofficial community project to provide a package that's easy to
install on Debian. If you're looking for the starship source code, see
[starship](https://github.com/starship/starship).

## Install/Update

### The Debian way

```sh
sudo install -d -m 0755 /etc/apt/keyrings
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.gpg -o /etc/apt/keyrings/deb.gaofn.xyz.gpg
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.sources -o /etc/apt/sources.list.d/deb.gaofn.xyz.sources
# Debian 12 (bookworm): fetch deb.gaofn.xyz-bookworm.sources instead
sudo apt update
sudo apt install -y starship
```

### Manual Installation

1. Download the .deb package for your Debian version available on
   the [Releases](https://github.com/gaofengnan/starship-debian/releases) page.
2. Install the downloaded .deb package.

```sh
sudo dpkg -i <filename>.deb
```
## Updating

To update to a new version, just follow any of the installation methods above. There's no need to uninstall the old version; it will be updated correctly.

## Building

### Build for single architecture
```sh
./build.sh <starship_version> <build_version> <architecture>
# Example: ./build.sh 1.2.3 1 arm64
```

### Build for all architectures
```sh
./build.sh <starship_version> <build_version> all
# Example: ./build.sh 1.2.3 1 all
```

## Roadmap

- [x] Produce a .deb package on GitHub Releases
- [x] Set up a debian mirror for easier updates
- [x] Multi-architecture support (amd64, arm64, armhf, i386, riscv64)

## Disclaimer

- This repo is not open for issues related to starship. This repo is only for _unofficial_ Debian packaging.
