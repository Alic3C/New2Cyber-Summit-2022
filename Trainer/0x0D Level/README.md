# 0x0D Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level11@trainer:~$ su - level12
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

Welcome to Level 12

For this level you are going to find SUID and SGID binaries in common locations.  This is a common privilege escalation technique seen in CTFs and real world.  Remember the user you are looking to escalate privileges to is level13.

type: man find
      google SUID
      google SGID

level12@trainer:~$ find / -perm -6000 -type f 2>/dev/null
/usr/sbin/mysecret

level12@trainer:~$ cd /usr/sbin

level12@trainer:/usr/sbin$ ./mysecret
f4736e1eb28b1d9055c5f5d58a49b5a6
```

## Flag
Flag: `f4736e1eb28b1d9055c5f5d58a49b5a6`