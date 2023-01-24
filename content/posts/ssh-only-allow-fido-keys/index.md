---
title: SSH Allow Only FIDO Keys To Login
date: 2023-01-24 10:11:01
category: notes
tags:
    - SSH
keywords:
    - ssh
---

## Introduction
If you have switched SSH keys to only using FIDO (sk-ssh-ed25519), then you can limit SSHD to only allow logins
from these key types.


## How To

Edit the sshd config to accept only sk-ssh-ed25519:

```shell
$ sudo vi /etc/ssh/sshd_config

PubkeyAcceptedKeyTypes sk-ssh-ed25519@openssh.com

$ sudo systemctl restart sshd

```

*If you have automated users connecting over ssh you may want to allow other key types as well, for example* `PubkeyAcceptedKeyTypes ssh-ed25519,sk-ssh-ed25519@openssh.com`
