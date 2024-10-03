# Matching with *

In this we are asked to use the concept of 'globbing'. the glob patterns specify sets of filenames with wildcard characters. We are asked to change directory to `/challenge` but not by typing in the entire thing but by using glob and the argument must not be longer than 4 characters. therefore running `cd /ch*` will successfuly complete the challenge.

```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{Ar6-abY9GPvTKezu1kVQ_w9WKBF.dFjM4QDLxITN0czW}
