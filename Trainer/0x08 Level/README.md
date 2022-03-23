# 0x08 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level6@trainer:~/dir13/subdir40$ su - level7
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

Welcome to Level 7


The password for the next level is in the password_directory.  For this level though, all files are exactly the same size.  You should look through each file to find the one that contains the password.

Hint: look for password

type: man find
      man grep
      man xargs

level7@trainer:~$ grep -r "password_directory" .
./welcome_message:The password for the next level is in the password_directory.  For this level though, all files are exactly the same size.  You should look through each file to find the one that contains the password.
./helpme:cd password_directory
./helpme:cd password_directory
./helpme:cd password_directory
./.viminfo:'0  6  4  ~/password_directory/search.sh
./.viminfo:|4,48,6,4,1648063062,"~/password_directory/search.sh"
./.viminfo:'1  3  27  ~/password_directory/level8_password68
./.viminfo:|4,49,3,27,1644089982,"~/password_directory/level8_password68"
./.viminfo:'2  1  0  ~/password_directory/test.sh
./.viminfo:|4,50,1,0,1644083755,"~/password_directory/test.sh"
./.viminfo:'3  3  27  ~/password_directory/level8_password68
./.viminfo:|4,51,3,27,1644083624,"~/password_directory/level8_password68"
./.viminfo:'4  4  0  ~/password_directory/level8_password68
./.viminfo:|4,52,4,0,1644083613,"~/password_directory/level8_password68"
./.viminfo:'5  4  0  ~/password_directory/level8_password68
./.viminfo:|4,53,4,0,1644083613,"~/password_directory/level8_password68"
./.viminfo:'6  4  0  ~/password_directory/level8_password68
./.viminfo:|4,54,4,0,1644083613,"~/password_directory/level8_password68"
./.viminfo:'7  4  0  ~/password_directory/level8_password68
./.viminfo:|4,55,4,0,1644083613,"~/password_directory/level8_password68"
./.viminfo:'8  6  4  ~/password_directory/search.sh
./.viminfo:|4,56,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:'9  3  16  ~/password_directory/search.sh
./.viminfo:|4,57,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1648063062,"~/password_directory/search.sh"
./.viminfo:-'  3  27  ~/password_directory/level8_password68
./.viminfo:|4,39,3,27,1644089982,"~/password_directory/level8_password68"
./.viminfo:-'  3  27  ~/password_directory/level8_password68
./.viminfo:|4,39,3,27,1644089982,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/test.sh
./.viminfo:|4,39,1,0,1644083755,"~/password_directory/test.sh"
./.viminfo:-'  1  0  ~/password_directory/test.sh
./.viminfo:|4,39,1,0,1644083755,"~/password_directory/test.sh"
./.viminfo:-'  1  0  ~/password_directory/test.sh
./.viminfo:|4,39,1,0,1644083755,"~/password_directory/test.sh"
./.viminfo:-'  1  0  ~/password_directory/test.sh
./.viminfo:|4,39,1,0,1644083755,"~/password_directory/test.sh"
./.viminfo:-'  3  27  ~/password_directory/level8_password68
./.viminfo:|4,39,3,27,1644083624,"~/password_directory/level8_password68"
./.viminfo:-'  3  27  ~/password_directory/level8_password68
./.viminfo:|4,39,3,27,1644083624,"~/password_directory/level8_password68"
./.viminfo:-'  3  27  ~/password_directory/level8_password68
./.viminfo:|4,39,3,27,1644083624,"~/password_directory/level8_password68"
./.viminfo:-'  3  27  ~/password_directory/level8_password68
./.viminfo:|4,39,3,27,1644083624,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083619,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083619,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083619,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083619,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083619,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083619,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083613,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083613,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083613,"~/password_directory/level8_password68"
./.viminfo:-'  4  0  ~/password_directory/level8_password68
./.viminfo:|4,39,4,0,1644083613,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  1  0  ~/password_directory/level8_password68
./.viminfo:|4,39,1,0,1644083607,"~/password_directory/level8_password68"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  6  4  ~/password_directory/search.sh
./.viminfo:|4,39,6,4,1644083028,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082927,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  16  ~/password_directory/search.sh
./.viminfo:|4,39,3,16,1644082887,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1643996001,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1636222566,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1636222566,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1636222566,"~/password_directory/search.sh"
./.viminfo:-'  3  18  ~/password_directory/search.sh
./.viminfo:|4,39,3,18,1636222566,"~/password_directory/search.sh"
./.viminfo:> ~/password_directory/search.sh
./.viminfo:> ~/password_directory/level8_password68
./.viminfo:> ~/password_directory/test.sh
level7@trainer:~$ cd password_directory
level7@trainer:~/password_directory$ cat level8_password68
The password for level8 is:

bGV0J3MgZmluZCBzb21ldGhpbmcg

```

## Flag
Flag: `bGV0J3MgZmluZCBzb21ldGhpbmcg`