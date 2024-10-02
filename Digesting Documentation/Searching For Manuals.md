# Searching For Manuals.md

In this challenge we need to read the manual of `/challenge/challenge` but it has been renamed thus we need to read the manual of the `man` command itself to look for clues that might help us find the renamed manual for `/challenge/challenge`.

I started off by reading the manual for `man`. and in its manual the following argument seemed promising:
```bash
-k, --apropos
              Equivalent  to  apropos.   Search the short manual page descrip‐
              tions for keywords and display any matches.  See apropos(1)  for
              details.
```
the -k argument helps us by displaying matches for the entered keywords. Hence, executing `challenge` as `-k`'s argument seemed promising. 
```bash
hacker@man~searching-for-manuals:~$ man -k challenge
qcnjwkctkb (1)       - print the flag!
```
Thus we found out the renamed manual for `/challenge/challenge`. Now all we need to do is read this manual page to find which argument prints the flag.
```bash
hacker@man~searching-for-manuals:~$ man qcnjwkctkb

CHALLENGE(1)                                                                              Challenge Commands                                                                              CHALLENGE(1)

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

       --qcnjwk NUM
              print the flag if NUM is 964

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                                                                    May 2024
                                                 CHALLENGE(1)
```
Thus the `--qcnjwk NUM` will return the required flag when `NUM` is `964`
```bash
hacker@man~searching-for-manuals:~$ /challenge/challenge --qcnjwk 964
Correct usage! Your flag: pwn.college{AN_qRcUnBX9j6AwCkctB_kbJTYs.dZTM4QDLxITN0czW}
```
