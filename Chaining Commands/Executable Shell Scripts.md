# Executable Shell Scripts
When we use `bash script.sh` we are explicitly telling the system to run `script.sh` using the `bash` shell. However if we directly make our shell script an executable we can directly run it without needing to specify `bash`. AS per the challenge we need to store the command `/challenge/solve` in a shell script then make that shell script a executable and run it to get our flag.

# My Solve
Firstly I did `echo /challenge/solve > x.sh` to store `/challenge/solev` in a script shell named `x.sh` then i viewed the permissions of `x.sh` using `ls -l x.sh` after that i did `chmod u+x x.sh` which gave us, the hacker, executing permissions of `x.sh`. After that we simply executed the shell script using `./x.sh` to get our flag.
```bash
hacker@chaining~executable-shell-scripts:~$ echo /challenge/solve > x.sh
hacker@chaining~executable-shell-scripts:~$ ls -l x.sh
-rw-r--r-- 1 hacker hacker 17 Oct 14 18:43 x.sh
hacker@chaining~executable-shell-scripts:~$ chmod u+x x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{oOdWqxfjx3iZ7Do7RzRFblOEzbF.dRzNyUDLxITN0czW}
