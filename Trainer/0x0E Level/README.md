# 0x0E Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level12@trainer:/usr/sbin$ su - level13
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

Welcome to Level 13

For this level you are going to familiarize yourself with environment variables.  They are used for a wide variety of applications.  Specifically, they can be used for docker and cloud providers to store credentials.  They password to level 14 is for Amazon and is the one that ends with ID.

type: man environ
      google environment variables

level13@trainer:~$ env | grep ID
AWS_ACCESS_KEY_ID=0ea027e3835aa87a4a47465321c5fe75
```

## Flag
Flag: `0ea027e3835aa87a4a47465321c5fe75`