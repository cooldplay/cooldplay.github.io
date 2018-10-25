---
title: SSH Keypair 생성하기
layout: post
---

```bash
ssh-keygen -N "" -f /home/$USER/.ssh/id_rsa  # No passphrase
ssh-agent /bin/bash
ssh-add ~/.ssh/id_rsa
ssh-add -l
```
