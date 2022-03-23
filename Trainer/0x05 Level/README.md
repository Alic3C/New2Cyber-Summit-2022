# 0x05 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level3@trainer:~$ su - level4
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

Welcome to Level 4

The password for the next level is in this user's home directory, just like the last levels you might have to dig.

type: man ls    read about files and folders that start with a dot (.)

level4@trainer:~$ ls -a
 .    .bash_logout              .gnupg        .local    ls-a       .vim
 ..   .bashrc                   helpme       'ls - a'   .profile   .viminfo
 -a   .cloud-locale-test.skip   .hidden_dir  'ls -a'    .ssh       welcome_message
level4@trainer:~$ cd .hidden_dir/
level4@trainer:~/.hidden_dir$ ls -a
 .   ..   .level5_password  'ls -a'
level4@trainer:~/.hidden_dir$ cat .level5_password
7b6c2552940f47a27fbd729ae0e2893c
```

## Flag
Flag: `7b6c2552940f47a27fbd729ae0e2893c`