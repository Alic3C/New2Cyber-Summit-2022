# 0x06 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level4@trainer:~/.hidden_dir$ su - level5
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

Welcome to Level 5

For this level the password is in level6's home directory.  Due to a persmissions error, the level5 user can access it.  Think about the directories you have already seen and what file name patterns.

level5@trainer:~$ ls
level0   level11  level14  level17  level2   level22  level5  level8
level1   level12  level15  level18  level20  level3   level6  level9
level10  level13  level16  level19  level21  level4   level7  trainer
level5@trainer:/home$ cd level6
level5@trainer:/home/level6$ ls
0              dir13  dir19  dir24  dir3   dir35  dir40  dir46  dir6             pass
checklist.chk  dir14  dir2   dir25  dir30  dir36  dir41  dir47  dir7             welcome_message
dir1           dir15  dir20  dir26  dir31  dir37  dir42  dir48  dir8
dir10          dir16  dir21  dir27  dir32  dir38  dir43  dir49  dir9
dir11          dir17  dir22  dir28  dir33  dir39  dir44  dir5   helpme
dir12          dir18  dir23  dir29  dir34  dir4   dir45  dir50  level6_password
level5@trainer:/home/level6$ cat level6_password
7cb1963d316b9a302cf6c204d35b7302
```

## Flag
Flag: `7cb1963d316b9a302cf6c204d35b7302`