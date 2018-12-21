# st - simple terminal

This repo is a fork of [st](https://st.suckless.org) - a simple terminal emulator for X which sucks less.

## Requirements

In order to build st you need the `Xlib` header files.

## Installation

```sh
make
sudo make install
```

## Patches

Following [patches](https://st.suckless.org/patches/) are already applied:

- alpha - for transparent background
- anysize - makes the inner border size dynamic
- clipboard - enable copy after select text
- dracula - nice theme
- scrollback - scroll back through terminal output (`shift + PgUp/PgDn` or `shift + mouse wheel`)

To apply another patch use following command:

```sh
git apply -3 --ignore-whitespace /path/to/patch.diff
```

But be careful. When patch modifies `config.def.h` copy these changes to `config.h` and reset state of first file:

```sh
git reset HEAD config.def.h
git checkout -- config.def.h
```

Then repeat installation process.

## Sync with original st

Add `upstream` to original repo:

```sh
git remote add upstream git://git.suckless.org/st
```

Every time you want to sync type:

```sh
git fetch upstream
git checkout master
git merge upstream/master
```

This brings your `master` branch into sync with the upstream repository, without losing your local changes.
For reference check this [github article](https://help.github.com/articles/syncing-a-fork/)

Then repeat installation process.
