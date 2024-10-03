# Writing to multiple programs
In this challenge we executed the `/challenge/hack` command and used the `tee` command with process substitution to duplicate its output, sending it as input to both the `/challenge/the` and `/challenge/planet` commands simultaneously thus getting our required flag
```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
2477515133936122537
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
2620530498290799102
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{QWLJPGei52ysJsyIzzQB4F8k784.dBDO0UDLxITN0czW}
