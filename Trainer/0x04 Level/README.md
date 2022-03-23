# 0x04 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level2@trainer:~/dir/another_dir/another_another_dir/some_directory$ su - level3
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

Welcome to Level 3

The password for the next level is in this user's home directory, but you might not see it at first.

type: man ls    read about files that start with a dot (.)

level3@trainer:~$ ls -a
 .              .bashrc                   helpme                 .local     .ssh
 ..             .cloud-locale-test.skip   .lesshst              'ls -a'     tree
 -a             .config                   .level4_password       .profile   .viminfo
 .bash_logout   .gnupg                    .level4_password.swp   q          welcome_message
level3@trainer:~$ cat .level4_password
72f6af6b0005adb15fbc91e1b140115f
```

## Flag
Flag: `72f6af6b0005adb15fbc91e1b140115f`