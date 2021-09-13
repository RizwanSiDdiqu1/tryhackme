## Task 1 - Introduction
> You were hired as a SOC Analyst for one of the biggest Juice Shops in the world and an attacker has made their way into your network. 
> An IT team has sent you a zip file containing logs from the server. Download the attached file, type in "I am ready!" and get to work! There's no time to lose!
```
I am ready!
```
----------------------------------------------------------------

## Task 2 - Reconnaissance
> What tools did the attacker use? (Order by the occurrence in the log)
```bash
nmap,hydra,sqlmap,curl,feroxbuster
```
> What endpoint was vulnerable to a brute-force attack?
```url
rest/user/login
```
> What endpoint was vulnerable to SQL injection?
```
/rest/products/search?q=
```
> What parameter was used for the SQL injection?
```
q
```
> What endpoint did the attacker try to use to retrieve files? (Include the /)
```
/ftp
```
-----------------------------------------------------------
## Task 3 - Stolen data
> What section of the website did the attacker use to scrape user email addresses?
```
products reviews
```
> Was their brute-force attack successful? If so, what is the timestamp of the successful login? (Yay/Nay, 11/Apr/2021:09:xx:xx +0000)
```
Yay,11/Apr/2021:09:16:31+0000
```
> What user information was the attacker able to retrieve from the endpoint vulnerable to SQL injection?
```
email,password
```
> What files did they try to download from the vulnerable endpoint? (endpoint from the previous task, question #5)
```
www-data.bak,coupons_2013.md.bak
```
> What service and account name were used to retrieve files from the previous question? (service, username)
```
ftp,anonymous
```
> What service and username were used to gain shell access to the server? (service, username)
```
ssh,www-data
```
