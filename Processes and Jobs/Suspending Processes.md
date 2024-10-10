# Suspending Processes
In this challenge we need to use `Ctrl+Z` to suspend a particular application which allows us to open another version of the same application or do anything else in the terminal.

# My Solve
As per the challenge we need to run `/challenge/run` then suspend it using `Ctrl+Z` then again run the same file so that there exists two versions of the same file simultaneously which should then give us the required flag.
```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 14:43 pts/0    00:00:00 bash /challenge/run
root          84      82  0 14:43 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 14:43 pts/0    00:00:00 bash /challenge/run
root          89      65  0 14:43 pts/0    00:00:00 bash /challenge/run
root          91      89  0 14:43 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{YBnib23CrxtkwVJEF_XrD0U5bXd.dVDN4QDLxITN0czW}
