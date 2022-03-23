# 0x07 Level
> 10pts

## Category
> Linux

## Briefing
> The password to level

> Note: Not the standard flag format

## Solution
```console
level5@trainer:/home/level6$ su - level6
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

Welcome to Level 6

The password for the next level is in this user's home directory, however this time there are too many directories to manually dig through.  For this level you will need the find command and search for a file that has pass in the title.

type: man find    read searching for filenames


level6@trainer:~$ grep -r "pass" .
./pass:       Search for files, directories, and symbolic links in the directory /tmp passing these types as a comma-separated list (GNU extension), which is otherwise equivalent to the longer, yet more portable:
./pass:       This happens when the shell could expand the pattern *.c to more than one file name existing in the current directory, and passing the resulting file names in the command line tod like this:
./dir13/subdir40/level7_password:The password for level7 is:
./welcome_message:The password for the next level is in this user's home directory, however this time there are too many directories to manually dig through.  For this level you will need the find command and search for a file that has pass in the title.
./checklist.chk:e0aef31024b5de9df6b3be6169854a9e  ./pass
./checklist.chk:6f692e7cb700ba33cea7a2c5b64ac06e  ./dir13/subdir40/level7_password
./checklist.chk:07bd5a26a0566bfe964380201ce6d495  ./level6_password
./helpme:password.  find has an option -name where you can specify the name
./helpme:of the file.  All we know is that there is password in the title, so
./helpme:we are going to wildcard the beginning and end of password with *
./helpme:find . -name *password*
./helpme:find . | grep password
./helpme:cat ./dir13/subdir40/level7_password
./.viminfo:~MSle0~/pass
./.viminfo:?/pass
./.viminfo:|2,1,1644092683,47,"pass"
./.viminfo:'0  13  7  ~/pass
./.viminfo:|4,48,13,7,1644095054,"~/pass"
./.viminfo:'1  883  0  ~/pass
./.viminfo:|4,49,883,0,1644093926,"~/pass"
./.viminfo:'2  883  0  ~/pass
./.viminfo:|4,50,883,0,1644093926,"~/pass"
./.viminfo:'3  876  87  ~/pass
./.viminfo:|4,51,876,87,1644092746,"~/pass"
./.viminfo:'4  876  87  ~/pass
./.viminfo:|4,52,876,87,1644092746,"~/pass"
./.viminfo:'5  876  87  ~/pass
./.viminfo:|4,53,876,87,1644092746,"~/pass"
./.viminfo:'6  876  87  ~/pass
./.viminfo:|4,54,876,87,1644092746,"~/pass"
./.viminfo:'7  1  0  ~/dir13/subdir40/level7_password
./.viminfo:|4,55,1,0,1644089691,"~/dir13/subdir40/level7_password"
./.viminfo:'9  2  0  ~/level6_password
./.viminfo:|4,57,2,0,1631694384,"~/level6_password"
./.viminfo:-'  13  7  ~/pass
./.viminfo:|4,39,13,7,1644095054,"~/pass"
./.viminfo:-'  883  0  ~/pass
./.viminfo:|4,39,883,0,1644095034,"~/pass"
./.viminfo:-'  883  0  ~/pass
./.viminfo:|4,39,883,0,1644093926,"~/pass"
./.viminfo:-'  876  87  ~/pass
./.viminfo:|4,39,876,87,1644093908,"~/pass"
./.viminfo:-'  876  87  ~/pass
./.viminfo:|4,39,876,87,1644093908,"~/pass"
./.viminfo:-'  876  87  ~/pass
./.viminfo:|4,39,876,87,1644092746,"~/pass"
./.viminfo:-'  941  136  ~/pass
./.viminfo:|4,39,941,136,1644092704,"~/pass"
./.viminfo:-'  941  136  ~/pass
./.viminfo:|4,39,941,136,1644092704,"~/pass"
./.viminfo:-'  941  136  ~/pass
./.viminfo:|4,39,941,136,1644092704,"~/pass"
./.viminfo:-'  134  0  ~/pass
./.viminfo:|4,39,134,0,1644092683,"~/pass"
./.viminfo:-'  134  0  ~/pass
./.viminfo:|4,39,134,0,1644092683,"~/pass"
./.viminfo:-'  134  0  ~/pass
./.viminfo:|4,39,134,0,1644092683,"~/pass"
./.viminfo:-'  1  0  ~/pass
./.viminfo:|4,39,1,0,1644092592,"~/pass"
./.viminfo:-'  1  0  ~/pass
./.viminfo:|4,39,1,0,1644092592,"~/pass"
./.viminfo:-'  1  0  ~/pass
./.viminfo:|4,39,1,0,1644092592,"~/pass"
./.viminfo:-'  1  0  ~/dir13/subdir40/level7_password
./.viminfo:|4,39,1,0,1644089691,"~/dir13/subdir40/level7_password"
./.viminfo:-'  1  0  ~/dir13/subdir40/level7_password
./.viminfo:|4,39,1,0,1644089691,"~/dir13/subdir40/level7_password"
./.viminfo:-'  1  0  ~/dir13/subdir40/level7_password
./.viminfo:|4,39,1,0,1644089691,"~/dir13/subdir40/level7_password"
./.viminfo:-'  1  0  ~/dir13/subdir40/level7_password
./.viminfo:|4,39,1,0,1644089691,"~/dir13/subdir40/level7_password"
./.viminfo:-'  1  0  ~/dir13/subdir40/level7_password
./.viminfo:|4,39,1,0,1644089691,"~/dir13/subdir40/level7_password"
./.viminfo:-'  1  0  ~/dir13/subdir40/level7_password
./.viminfo:|4,39,1,0,1644089691,"~/dir13/subdir40/level7_password"
./.viminfo:-'  1  0  ~/dir13/subdir40/level7_password
./.viminfo:|4,39,1,0,1644089691,"~/dir13/subdir40/level7_password"
./.viminfo:-'  1  0  ~/dir13/subdir40/level7_password
./.viminfo:|4,39,1,0,1644089691,"~/dir13/subdir40/level7_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  2  0  ~/level6_password
./.viminfo:|4,39,2,0,1631694384,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:-'  1  0  ~/level6_password
./.viminfo:|4,39,1,0,1631694371,"~/level6_password"
./.viminfo:> ~/pass
./.viminfo:> ~/dir13/subdir40/level7_password
./.viminfo:> ~/level6_password

level6@trainer:~$ cd dir13/subdir40
level6@trainer:~/dir13/subdir40$ cat level7_password
The password for level7 is:

RG8geW91IGV2ZW4gbGlmdCBicm8g
```

## Flag
Flag: `RG8geW91IGV2ZW4gbGlmdCBicm8g`