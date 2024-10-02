# Reading Manuals

In this challenge we need to learn how to use the `man` commmand which gives us the manual for the command passed as its argument. As per the challenge, we need to read the manual for `challenge` and in its manual we are instructed on how to get the flag.

### Manual
```bash
hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                  Challenge Commands                  CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --oroxro NUM
              print the flag if NUM is 445

AUTHOR
       Written by Zardus.
```
Thus as we can see from the manual to get the flag we must use the `--oroxro NUM` command with `445` as the `NUM`
```bash
hacker@man~reading-manuals:~$ /challenge/challenge --oroxro 445
Correct usage! Your flag: pwn.college{oroxUr4-otxYfMZj45Wd5pQTk0j.dRTM4QDLxITN0czW}
