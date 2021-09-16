## Task 1 - Mustacchio
- After enumerating I found user.bak file which give me admin password and online opner for [bak](https://filext.com/file-extension/BAK):
```
admin:1868e36a6d2b17d4c2745f1659433a54d4bc5f4b
```
- after decoding hash : `bulldog19`
- After loging in admin panel found this username : `Barry`
## Nmap Scan
```
22/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.10 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   2048 58:1b:0c:0f:fa:cf:05:be:4c:c0:7a:f1:f1:88:61:1c (RSA)
|   256 3c:fc:e8:a3:7e:03:9a:30:2c:77:e0:0a:1c:e4:52:e6 (ECDSA)
|_  256 9d:59:c6:c7:79:c5:54:c4:1d:aa:e4:d1:84:71:01:92 (ED25519)
80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
| http-robots.txt: 1 disallowed entry
|_/
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: Mustacchio | Home
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
Not shown: 65532 filtered ports
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
8765/tcp open  ultraseek-http
```
> What is the user flag?
```
62d77a4d5f97d47c5aa38b3b2651b831
```
> What is the root flag?
```
```
