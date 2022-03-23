# 0x0C Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level10@trainer:~$ su - level11
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

Welcome to Level 11

For this level you are given a file that contains the password to the next level.  The password is a md5 hash.  Research md5 hashes and find it in the file.

type: man grep
      man md5sum
      google md5 hash

level11@trainer:~$ grep -e "[0-9a-f]\{32\}" md5find
0982e2a869857644074d06b1a4fd1bea
```

## Flag
Flag: `0982e2a869857644074d06b1a4fd1bea`