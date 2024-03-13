# suForce

**Obtains a user's password by abusing the su binary.**

![](/screenshot.png)

- <kbd>Download suForce</kbd>

```sh
cd /dev/shm
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/suForce"
chmod +x suForce
```

- <kbd>Download Wordlist (Optional)</kbd>

```sh
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/techyou.txt"
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/top12000.txt"
```

- <kbd>Usage</kbd>

```cmd
./suForce -u <USER> -w <WORDLIST>
```

---
