# Executable Files
In this challenge we need to make use of the `chmod` command to make the `/flag` file executable by us.

We can recall that `u+rwx` gives all permissions to the owner user, `g+rwx` gives all permisssions to the group owner and `o+rwx` gives all permissions to other users.

# My Solve
Firstly i did `ls -l /challenge/run` to view info of `/challenge/run`, here we can see that the owner is us, the `hacker` thus giving executable permissions to the owner user will make it so that we can execute the file and get our flag. Doing `u+x` should do the job. After that we simply run the file to get our flag.
```bash
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r--r--r-- 1 hacker hacker 32 Jul  4 06:37 /challenge/run
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{EBJY-zFR8nulPj1HJ1Q9Ml4DKg3.dJTM2QDLxITN0czW}
