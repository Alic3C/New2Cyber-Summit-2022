# 0x14 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level18@trainer:~$ su - level19
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

Welcome to Level 19

For this level you are going to continue familiarizing yourself with user artifacts.  Look in this user's home directory to see if there are any files left behind that may contain useful information.

type: man ssh

level19@trainer:~$ ls -la ~/.ssh
total 28
drwxr-x--x 2 level19 level19 4096 Mar 23 21:14 .
drwxr-x--- 6 level19 level19 4096 Mar 23 22:56 ..
-rw-r--r-- 1 level19 level19    0 Sep 15  2021 config
-rw------- 1 level19 level19 2175 Mar 23 21:14 known_hosts
-rw-r--r-- 1 level19 level19  888 Nov  6 18:46 known_hosts.old
-rw------- 1 level19 level19 1823 Nov  6 19:42 level20_id
-rw-r--r-- 1 level19 level19  397 Nov  6 19:42 level20_id.pub
-rw------- 1 level19 level19 1811 Aug 23  2021 level20_id_rsa

level19@trainer:~$ scp level19@trainer.threatsims.com:~/.ssh/level20_id_rsa .
level19@trainer.threatsims.com's password:
level20_id_rsa                                                                                                                                                      100% 1811     5.6MB/s   00:00
level19@trainer:~$ ssh -i level20_id_rsa level20@trainer.threatsims.com
Linux trainer 4.19.0-19-cloud-amd64 #1 SMP Debian 4.19.232-1 (2022-03-07) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Wed Mar 23 23:10:35 2022 from 147.182.253.159

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

Welcome to Level 20

For this level you are going to continue familiarizing yourself with user artifacts.  Look in this user's home directory to see if there are any files left behind that may contain useful information.

type: man file
      man tar



level20@trainer:~$ cat level20_password
The password for level20 is:

5cf82d972614f73422f899f90cfce80f
```

## Flag
Flag: `5cf82d972614f73422f899f90cfce80f`