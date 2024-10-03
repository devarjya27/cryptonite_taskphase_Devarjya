# Duplicating piped data with tee

In this challenge we use the `tee` command to duplicate the output of a program to the terminal or a different file which might help us in debugging. What i did was use the `tee` command to store the output of `/challenge/pwn` in a file called `pwn` then i read that file to get the secret argument and then eventually get the flag.
```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "Y0VZHmRj"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret Y0VZHmRj | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{Y0VZHmRjHu1IHW48nZajBgztPlz.dFjM5QDLxITN0czW}
```
another not-so-fun fact: this took me, again, more than 40 mins to do 🤡 i had to look up how to use this command. i hated this. link to the resource i used: <https://tech-couch.com/post/understanding-the-linux-tee-command>
