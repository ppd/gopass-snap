# gopass-snap

Snap package for gopass: https://www.gopass.pw/

## Install

At the moment, due to lacking support in the ```gpg-keys``` interface,
gopass con only be used in devmode. This is hopefully only an intermediate
workaround.

```bash
snap install --devmode --beta gopass
```

## Snap specific things

### Default password store path

```$SNAP_USER_COMMON/password-store```, i.e. ```~/snap/gopass/common/password-store```

Custom paths can be set as required. However, the ```home``` interface does not
allow access to dot-prefixed top-level directories in the home directory.
