# 0x12 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level16@trainer:~$ su - level17
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

Welcome to Level 17

For this level you are going to familiarize yourself with user artifacts.  Look in this user's home directory to see if there are any files left behind that may contain useful information.

type: man vim

level17@trainer:~$ cat .viminfo
# This viminfo file was generated by Vim 8.1.
# You may edit it if you're careful!

# Viminfo version
|1,4

# Value of 'encoding' when this file was written
*encoding=utf-8


# hlsearch on (H) or off (h):
~h
# Command Line History (newest to oldest):
:wq
|2,0,1583196421,,"wq"

# Search String History (newest to oldest):

# Expression History (newest to oldest):

# Input Line History (newest to oldest):

# Debug Line History (newest to oldest):

# Registers:
"a      LINE    0
        ssh level18@localhost
|3,0,10,1,1,0,1583196413,"ssh level18@localhost"
""b     LINE    0
        9a42b1822710d790a393800f2896a8f7
|3,1,11,1,1,0,1583196418,"9a42b1822710d790a393800f2896a8f7"

# File marks:
'0  11  0  ~/password
|4,48,11,0,1583196421,"~/password"
'1  12  0  ~/password
|4,49,12,0,1583196243,"~/password"
'2  11  0  ~/password
|4,50,11,0,1583196243,"~/password"

# Jumplist (newest first):
-'  11  0  ~/password
|4,39,11,0,1583196421,"~/password"
-'  12  0  ~/password
|4,39,12,0,1583196368,"~/password"
-'  11  0  ~/password
|4,39,11,0,1583196243,"~/password"
-'  8  0  ~/password
|4,39,8,0,1583196224,"~/password"


# History of marks within files (newest to oldest):

> ~/password
        *       1583196420      0
        "       11      0
        ^       6       1
        .       6       1
        +       6       0
        +       3       7
        +       1       3
        +       11      0
        +       10      0
        +       9       0
        +       8       0
        +       12      0
        +       6       1
        a       1       0
        b       2       0
        c       3       0
        d       4       0
```

## Flag
Flag: `9a42b1822710d790a393800f2896a8f7`