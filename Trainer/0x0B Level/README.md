# 0x0B Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level9@trainer:~$ su - level10
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

Welcome to Level 10

For this level you are given a log file from the program fail2ban.  Fail2ban is used monitor log files for suspicious activity like too many failed logins.  It is commonly deployed for use with Apache or SSH.  After a configured number of attempts it will create an iptables (linux firewall) rule to block the ip from communicating with the device for a period of time.

The log file is located in your home directory and is called fail2ban.log.  The password to level 11 is the number of times 112.85.42.94 was banned.

type: man grep
      man wc

level10@trainer:~$ grep -o 'Ban 112.85.42.94' fail2ban.log | wc -l
192
```

## Flag
Flag: `192`