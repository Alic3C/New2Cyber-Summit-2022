# 0x03 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level1@trainer:~/some_directory$ su - level2
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

Welcome to Level 2

The password for the next level is in this user's home directory, but you have to dig even deeper.

level2@trainer:~$ ls
dir  helpme  welcome_message
level2@trainer:~$ cd dir
level2@trainer:~/dir$ ls
another_dir
level2@trainer:~/dir$ cd another_dir/
level2@trainer:~/dir/another_dir$ ls
another_another_dir
level2@trainer:~/dir/another_dir$ cd another_another_dir/
level2@trainer:~/dir/another_dir/another_another_dir$ ls
some_directory
level2@trainer:~/dir/another_dir/another_another_dir$ cd some_directory/
level2@trainer:~/dir/another_dir/another_another_dir/some_directory$ ls
level3_password
level2@trainer:~/dir/another_dir/another_another_dir/some_directory$ cat level3_password
2cadca6148093c403d82396252b8c4db
```

## Flag
Flag: `2cadca6148093c403d82396252b8c4db`