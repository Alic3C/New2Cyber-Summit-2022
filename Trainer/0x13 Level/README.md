# 0x13 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level17@trainer:~$ su - level18
Password:

    ====================================================================
    ||                                                                ||
    ||     .--.          Welcom to the Linux Trainer!                 ||
    ||    | o_o|                                                      ||
    ||    | ==>|          To view the level instructions again        ||
    ||   / /   \ \         type: cat welcome_message                  ||
    ||  ( |     | )                                                   ||
    || /' |_____/'\       Getting Stuck? Need help with a level?      ||
    || \___)--(___/         type:  cat helpme                         ||
    ||                                                                ||
    ||                    Use "su - level#"  to change levels         ||
    ||                                                                ||
    ||                    feedback: nopresearcher@gmail.com           ||
    ||                                                                ||
    ||                                                                ||
    ====================================================================

Welcome to Level 18

For this level you are going to continue familiarizing yourself with user artifacts.  Look in this user's home directory to see if there are any files left behind that may contain useful information.

type: man bash

level18@trainer:~$ cat ~/.bash_history

whoami
uanme -a
w
id
ps -ef
netstat -an
cat /proc/version
cat /etc/*-release
pwd
ls -la
cat /etc/profile
cat ~/.bashrc
awk -F ":" '!/nologin/{print $1}' /etc/passwd
find / -perm -g=s -type f 2>/dev/null
ssh level19@localhost
b06a246b0646b337f319316b9232151c
whoami
ssh level19@127.0.0.1
pwd
ls -la
```

## Flag
Flag: `b06a246b0646b337f319316b9232151c`