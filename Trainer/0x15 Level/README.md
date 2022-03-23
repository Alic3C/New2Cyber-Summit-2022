# 0x15 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level20@trainer:~$ ls
backup.tar  backup.tgz  helpme  level20_password  level21_password  level21_password.bak  welcome_message

level20@trainer:~$ file backup.tgz
backup.tgz: POSIX tar archive

level20@trainer:~$ tar xvf backup.tgz
level21_password

level20@trainer:~$ cat level21_password
65230da2ead4ba2ed76ee2605cadcd4d
```

## Flag
Flag: `65230da2ead4ba2ed76ee2605cadcd4d`