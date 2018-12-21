## st - simple terminal

This repo is a fork of [st](https://st.suckless.org) - a simple terminal emulator for X which sucks less.

## Requirements

In order to build st you need the `Xlib` header files.

## Installation

```sh
make
sudo make install
```

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
