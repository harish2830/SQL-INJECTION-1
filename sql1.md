SQLI is also know as SQL Injection 

An SQL injection is a computer attack in which malicious code is added in a poorly-designed application
and then passed to the backend database. 
The malicious data then produces database query results or actions that should never have been executed.

How does SQLI works?

* In Order to run malicious SQL queries against a db server, 
An attacker must first find an input within the web application that is included inside of an SQL query.

* In order for an SQLI attack to take place the vulnrable website needs to directly include user inputs within an SQL statement.
AN attacker can then insert a playload that will be included as part of the SQL query and run against the database server.

SQL injection is mainly based on four types:

* SQLI can be GET based
* SQLI can be POST based
* SQLI can be HEADER based
* SQLI can be COOKIE based

##### SQLI can be GET based

Here attackers try to attack through URLS parameters .

ex1: domainname.com/filename.programming?parameter=value

ex2: http://www.domainname.com/index.php?id=1

##### SQLI can be POST based

Here attackers have to find any html form that may excute SQLI query 

ex: sign up form, login form, password reset from etc.

##### SQLI can be Header based.

Here attackers have to attack through headers parameters such as Referrer | User-Agent | Location | Host

##### SQLI can be COOKIE based.

Here attackers have to attack on cookies parameters 

ex: Cookie: username=hfsfjhfs;

### How to identify a website has SQL vulunerable : 

Just give simple keys like \ , ' , " , in url or login coloums, It shown an error on that page clearly as below screen shot

![image](/screenshots/SQL0.png)

### SQLI query fixing:

Identify SQLI vulnerability using 
'
"
\
balance the query

http://berkeleyrecycling.org/page.php?id=1 {front end}

select id='id' where name='xyz' {backend}








