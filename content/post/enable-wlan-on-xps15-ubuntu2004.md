---
title: "Ubuntu 20.04 で XPS-15-9530 の WLAN が認識されないときの対処法"
date: 2023-05-21T11:39:00+09:00
tags: ["Ubuntu", "XPS-15-9530", "トラブルシューティング"]
draft: false
---


## 方法1

以下をコピーして、ターミナルにペーストし、実行する。

```bash
sudo apt update
sudo apt install git
sudo apt install build-essential
git clone https://git.kernel.org/pub/scm/linux/kernel/git/iwlwifi/backport-iwlwifi.git
cd backport-iwlwifi
make defconfig-iwlwifi-public
make -j16
sudo make install
```

## 方法2

「[Ubuntu 20.04 の Kernel をアップデートする](/post/update-ubuntu2004-kernel/)」を参考にカーネルをアップデートする。