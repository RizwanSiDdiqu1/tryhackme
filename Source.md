#### Description : **Enumerate and root the box attached to this task. Can you discover the source of the disruption and leverage it to take control?**
![image](https://i.imgur.com/bgksoKQ.jpg)
## Nmap Scan
```PORT      STATE SERVICE VERSION
22/tcp    open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   2048 b7:4c:d0:bd:e2:7b:1b:15:72:27:64:56:29:15:ea:23 (RSA)
|   256 b7:85:23:11:4f:44:fa:22:00:8e:40:77:5e:cf:28:7c (ECDSA)
|_  256 a9:fe:4b:82:bf:89:34:59:36:5b:ec:da:c2:d3:95:ce (ED25519)
10000/tcp open  http    MiniServ 1.890 (Webmin httpd)
|_http-title: Site doesn't have a title (text/html; Charset=iso-8859-1).
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
```
## Task 1 get user.txt
```THM{SUPPLY_CHAIN_COMPROMISE}```
## Task 2 get root.txt
```THM{UPDATE_YOUR_INSTALL}```

