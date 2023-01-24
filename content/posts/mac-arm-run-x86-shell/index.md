---
title: MacOS Arm - Run x86_64 Shell
date: 2023-01-24 14:20:01
category: notes
tags:
    - Arm
    - Mac
keywords:
    - arm
    - mac
---

## Introduction 

If you need to run a binary or script that only works with x86_64, for example a old version of terraform with no
Arm binary, you can use `arch` to run a version under Rosetta.

## How To

```shell
arch -x86_64 /bin/zsh
```

Opens a ZSH shell running under x86

```shell
➜ uname -a
Darwin MBP 22.3.0 Darwin Kernel Version 22.3.0: Thu Jan  5 20:48:54 PST 2023; root:xnu-8792.81.2~2/RELEASE_ARM64_T6000 arm64

➜ arch -x86_64 /bin/zsh

➜ uname -a
Darwin MPB 22.3.0 Darwin Kernel Version 22.3.0: Thu Jan  5 20:48:54 PST 2023; root:xnu-8792.81.2~2/RELEASE_ARM64_T6000 x86_64
```