# Redirecting Script Output
We can also use the piping command `|` to redirect the output of our shell script if required. As per the challenge we need to create a shell script containing `/challenge/pwn` and `/challenge/college` and we need to redirect the output of the shell script to `/challenge/solve`.

# My Solve
Firstly I did `echo /challenge/pwn > x.sh` and `echo /challenge/college >> x.sh` to store the two commands in a shell script named `x.sh` after which i did `bash x.sh | /challenge/solve`, `bash x.sh` runs the shell script and `|` redirects that output to `/challenge/solve` which is what we require.
```bash
hacker@chaining~redirecting-script-output:~$ echo /challenge/pwn > x.sh
hacker@chaining~redirecting-script-output:~$ echo /challenge/college >> x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{cb00y3bZ4fZxLYg2XX4RBbdEpeU.dhTM5QDLxITN0czW}
