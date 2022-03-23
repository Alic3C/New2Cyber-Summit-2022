# 0x01 Level
> 10pts

## Category
> Linux

## Briefing
> SSH to the linux trainer:

> trainer.threatsims.com

> Note: This is not a web based link, it's an SSH host and you can connect to it via SSH protocol with tool such as PuTTY (google), or in linux use the ssh command.

> username: level0 password: level0

> After logging in to level0 you will be looking for the password to level1.

> The flag is always for the level in the challenge name. You will find it by completing the previous level.

> The password will be the login to level1

> Note: Not the standard flag format

## Solution
```console
CDSkids@kali:~/Desktop$ ssh level0@trainer.threatsims.com
level0@trainer.threatsims.com's password:
Linux trainer 4.19.0-19-cloud-amd64 #1 SMP Debian 4.19.232-1 (2022-03-07) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Wed Mar 23 20:24:38 2022 from 2.125.5.80

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

Welcome to Level 0

The password for the next level is in this user's home directory

level0@trainer:~$ cat level1_password
4202c26842398c1d0772ed9eed195113
```

## Flag
Flag: `4202c26842398c1d0772ed9eed195113`