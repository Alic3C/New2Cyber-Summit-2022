# 0x02 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level0@trainer:~$ su - level1
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

Welcome to Level 1

The password for the next level is in this user's home directory, but you may have to dig a bit.

level1@trainer:~$ ls
helpme  some_directory  welcome_message
level1@trainer:~$ cd some_directory/
level1@trainer:~/some_directory$ ls
level2_password  maybe
level1@trainer:~/some_directory$ cat level2_password
943430e07fd566bc96aa05fca3c96e48
```

## Flag
Flag: `943430e07fd566bc96aa05fca3c96e48`