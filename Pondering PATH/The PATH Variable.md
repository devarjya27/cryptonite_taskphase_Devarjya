# The Path Variable
When we run a command like `ls` or `rm`, the shell looks for the program in the directories specified by the `PATH` variable. As per the challenge, we need to prevent `/challenge/run` program from finding and executing the `rm` command which would delete the flag.

# My Solve
Firstly I did `ls` to see that `PATH` indeed does have certain directories specified which allows `ls` to run properly. Now if we set the `PATH` variable to nothing `ls` or `rm` in this case wont work as intended causing `/challenge/run` to not delete the flag. Thus we modify `PATH` by doing `PATH=""` after which we confirm that `ls` indeed does not work. After that we simply run `/challenge/run` to get the flag.
```bash
hacker@path~the-path-variable:~$ ls
COLLEGE  a            instructions  not-the-flag  the-flag
PWN      firstoutput  myflag        pwn           x.sh
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ ls
ssh-entrypoint: ls: No such file or directory
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{omv5eAzulVgG4-Px25UxPsLhGW7.dZzNwUDLxITN0czW}
