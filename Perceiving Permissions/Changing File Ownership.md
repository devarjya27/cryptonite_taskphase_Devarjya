# Changing File Ownership
In this challenge we need to use the `chown` command to change ownership for certain files. `chown` can only be invoked by the `root` user but as per the challenge we have the access to change the owner for the files even though we are not the `root` user. We are currently `hacker` so changing the ownership to `hacker` will allow us to do anything we want with the file. We can check the permissions of a file or a directory using `ls -l` and following it up with a file as an argument will give us the permissions for that particular file.

# My Solve
As per the challenge we need to change the owner of `/flag` to `hacker` instead of `root` then doing `cat flag` should give us the flag. Firstly I did `ls -l` to check permissions for the current directory. Then in the terminal we can see that there is no info for `/flag` thus passing `/flag` as a parameter in `ls -l` will tell us about the permissions for `/flag`. And then we invoke `chown` to change ownership to `hacker`. then we simply read the file to get our flag.

```bash
hacker@permissions~changing-file-ownership:~$ ls -l
total 28
-rw-r--r-- 1 hacker hacker   4 Oct  3 16:52 COLLEGE
-rw-r--r-- 1 hacker hacker   8 Oct  3 17:20 PWN
-rw-r--r-- 1 hacker hacker  58 Oct  1 13:21 a
-rw-r--r-- 1 hacker hacker   0 Oct  3 17:41 firstoutput
-rw-r--r-- 1 hacker hacker 829 Oct  3 17:15 instructions
-rw-r--r-- 1 hacker hacker  93 Oct  3 17:15 myflag
lrwxrwxrwx 1 hacker hacker   5 Oct  2 07:23 not-the-flag -> /flag
-rw-r--r-- 1 hacker hacker  77 Oct  3 17:54 pwn
-rw-r--r-- 1 hacker hacker 435 Oct  3 17:08 the-flag
hacker@permissions~changing-file-ownership:~$ ls -l /flag
-r-------- 1 root root 58 Oct 13 09:36 /flag
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ ls -l /flag
-r-------- 1 hacker root 58 Oct 13 09:36 /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{AD_55tVHuoAXilsQdVqqvHL_Z4m.dFTM2QDLxITN0czW}
