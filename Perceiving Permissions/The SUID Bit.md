# The SUID Bit
In this challenge we need to use the concept of `SUID` which stands for SET USER ID. The SUID bit allows a program to run with the privileges of its owner. We can set a file's `SUID` bit by doing `chmod u+s`. The `s` part in place of the executable bit means that the program is executable with `SUID`. As per the challenge we need to add the `SUID` bit to the `/challenge/getroot` program in order to spawn a root shell which will help us read `/flag` and get our flag.

# My Solve
Firstly I viewed the permissions for `/challenge/getroot` and confirmed that it does not have the `SUID` bit then I added the `SUID` bit by doing `chmod u+s /challenge/getroot` after which i ran the file which gave us the secret shell. In that shell i simply read `/flag` using `cat` to get the flag.
```bash
hacker@permissions~the-suid-bit:~$ ls -l /challenge/getroot
-rwxr-xr-x 1 root root 155 Jul 12 10:30 /challenge/getroot
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ ls -l /challenge/getroot
-rwsr-xr-x 1 root root 155 Jul 12 10:30 /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{YB1aH2dLDs97k47KYIW-JlURfdo.dNTM2QDLxITN0czW}
