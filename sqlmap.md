#### Using SQLMAP tool and Burp suite we are going to attack and retreat data from our created website(http://phone.com/index.php)


Check for SQL Vulnerablity in targeted website if yes then proceed with following process 

use simple payloads to make sure site is vulnerable. 

### Step 1.
 
Open Browser and take your targeted website and give some random username and password and wait to hit login 

screen shotb1

### Step 2.

Now turn on your Burp suite, make your intercept on to capture your login page session and go to browser and click on login this session will be capture by Burp suite save that captured session as a file(sql1) on desktop (convenent floder).


### Step 3.

Check for SQL Vulnerablity in targeted website if yes then proced with following process 

Now open sqlmap tool in your system terminal.

(Please go to this link for installation of SQLMAP tool in kali linux)

(will update link shortly)

>sqlmap

screenshot 1

>sqlmap -r sql1 http://phone.com/index.php -dbs

-r   --  stands for
sql1 --  saved file name 
http://phone.com/index.php --  Targeted website 
dbs  --  Databases

Give Yes to all search fields. 
then if its is vulnerable then you can see as below

screen 2

>sqlmap -r sql1 http://phone.com/index.php -D phone -T users --dump

In this above command sqlmap search all kind of parameters.

D - Database 
phone - Database name
T     -  Table
users - Tale names
dump  - dumping total data in table called users.

screen 3
screen 4






