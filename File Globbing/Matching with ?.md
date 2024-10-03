# Matching with ?
In this challenge, unlike the last challenge where we matched file names with `*`, we will be matching them with `?` but `?` matches with only a single character. `?` works as a placeholder for a single character whereas `*` acted as a placeholder for more than 1 character.
We are asked to change directories to `/challenge` but without typing in `c` and `l` thus we replace them with `?`.

```bash
his challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{Am2npePUIWVYcqvKKsGWAayF-5J.dJjM4QDLxITN0czW}
