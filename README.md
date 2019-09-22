# gopass-snap

Snap package for gopass: https://www.gopass.pw/

The packaging is work-in-progress and makes certain compromises owing to the sandboxed nature of snap apps.

## Installation

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/gopass)

or 

```bash
snap install gopass --edge
```

## Connecting Interfaces

Two interfaces are necessary for operation that are not auto-connected by snapd.

```bash
snap connect gopass:gpg-keys
snap connect gopass:ssh-keys
```

## Store Location (GOPASS_HOMEDIR)

Atm, the default store and config location is not `$HOME`, but `$HOME/gopass`.

