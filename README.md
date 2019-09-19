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

## Native Messaging Manifests for Browsers

Do not use `gopass jsonapi configure` to install the manifests, it is not suitable for the snap package.

### Firefox

```bash
mkdir -p ~/.mozilla/native-messaging-hosts
gopass.firefox-manifest | tee > ~/.mozilla/native-messaging-hosts/com.justwatch.gopass.json
```

### Chrome

```bash
mkdir -p ~/.config/google-chrome/NativeMessagingHosts
gopass.chrome-manifest | tee > ~/.config/google-chrome/NativeMessagingHosts/com.justwatch.gopass.json
```

### Chromium

```bash
mkdir -p ~/.config/chromium/NativeMessagingHosts
gopass.chrome-manifest | tee > ~/.config/chromium/NativeMessagingHosts/com.justwatch.gopass.json
```
