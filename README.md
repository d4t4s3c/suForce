# suForce

![GitHub stars](https://img.shields.io/github/stars/d4t4s3c/suForce?logoColor=yellow) ![GitHub forks](https://img.shields.io/github/forks/d4t4s3c/suForce?logoColor=purple) ![GitHub watchers](https://img.shields.io/github/watchers/d4t4s3c/suForce?logoColor=green)</br>
![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/m/d4t4s3c/suForce) ![GitHub contributors](https://img.shields.io/github/contributors/d4t4s3c/suForce)

## Overview

If you have a **username** and want to try to obtain their **password**, `suForce` will make authentication attempts against that user from the [su](https://manpages.ubuntu.com/manpages/xenial/man1/su.1.html) binary, performing a **brute force** attack until a successful collision occurs.

![](/img/img.png)

---

## Download

```sh
cd /dev/shm
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/refs/heads/main/suForce"
chmod +x suForce
```

## Usage

```sh
./suForce -u <USER> -w <WORDLIST>
```

---
