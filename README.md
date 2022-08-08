# asdf-gonogo

[![Build Status](https://travis-ci.org/TheCubicleJockey/asdf-gonogo.svg?branch=master)](https://travis-ci.org/TheCubicleJockey/asdf-gonogo)

gonogo plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Install

```
asdf plugin-add gonogo https://github.com/TheCubicleJockey/asdf-gonogo.git
```

## Use

Check out the [asdf documentation](https://asdf-vm.com/#/core-manage-versions?id=install-version) for instructions on how to install and manage versions of gonogo.

## Architecture Override
The `ASDF_gonogo_OVERWRITE_ARCH` variable can be used to override the architecture that is used for determining which `gonogo` build to download. The primary use case is when attempting to install an older version of `gonogo` for use on an Apple M1 computer as `gonogo` was not built for ARM at the time.

### Without `ASDF_gonogo_OVERWRITE_ARCH`:

```
% asdf install gonogo 1.24.3
Downloading gonogo from https://storage.googleapis.com/kubernetes-release/release/v1.18.17/bin/darwin/arm64/gonogo
```

### With `ASDF_gonogo_OVERWRITE_ARCH`:

```
% ASDF_gonogo_OVERWRITE_ARCH=amd64 asdf install gonogo 1.18.17
Downloading gonogo from https://storage.googleapis.com/kubernetes-release/release/v1.18.17/bin/darwin/amd64/gonogo
```

