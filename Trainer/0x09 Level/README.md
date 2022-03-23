# 0x09 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level7@trainer:~/password_directory$ su - level8
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

Welcome to Level 8

For this level the password is in an executable hidden in one of these sub-directories.  When you run the executable it will print out the flag.  To run the executable type: ./executable

type: man find

After finding and executing the binary, you should try to run the command strings on the it and review the output.  type: strings <executable>

level8@trainer:~$ find . -type f -executable
./dir24/subdir13/level9_password
level8@trainer:~$ cd dir24/subdir13
level8@trainer:~/dir24/subdir13$ ./level9_password
The password is: 96ab15e954f1267ea04c35de2d771c2b
```

## Flag
Flag: `96ab15e954f1267ea04c35de2d771c2b`