## Task 1 : Reconnaissance
- **Description** : *You're presented with a machine. Your first step should be recon. Scan the machine with nmap, work out what's running.*
## Nmap Scan 
```
Nmap scan report for 10.10.57.218
Host is up (0.33s latency).
Not shown: 997 closed ports
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   2048 10:a6:95:34:62:b0:56:2a:38:15:77:58:f4:f3:6c:ac (RSA)
|   256 6f:18:27:a4:e7:21:9d:4e:6d:55:b3:ac:c5:2d:d5:d3 (ECDSA)
|_  256 2d:c3:1b:58:4d:c3:5d:8e:6a:f6:37:9d:ca:ad:20:7c (ED25519)
80/tcp   open  http    Golang net/http server (Go-IPFS json-rpc or InfluxDB API)
|_http-title: Home - hackerNote
8080/tcp open  http    Golang net/http server (Go-IPFS json-rpc or InfluxDB API)
|_http-open-proxy: Proxy might be redirecting requests
|_http-title: Home - hackerNote
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
```
- Which ports are open? (in numerical order)
``` 22,80,8080 ```
- What programming language is the backend written in?
``` Go ```
## Task 2 - Exploit
- How many usernames from the list are valid?
```
1
```
- What are/is the valid username(s)?
```
james
```
- ssh jame's passowrd :
```
dak4ddb37b
```
- How many passwords were in your wordlist?
```
180
```
- What was the user's password?
```
blue7
```
- What's the user flag?
```
thm{56911bd7ba1371a3221478aa5c094d68}
```
## Task 3 - Esclate
- What is the CVE number for the exploit?
```
CVE-2019-18634
```
- What is the root flag?
```
thm{af55ada6c2445446eb0606b5a2d3a4d2}
```

