# home sweet home

In this challenge we invoke `/challenge/run` followed by a file specified as an argument which will store the flag upon correct execution of the program. Thus all we need to do is type in `/challenge/run ~/a`, here `~/a` refers to `/home/hacker/a`. Thus satisfying all the given constraints. The argument is an absolute path - `/home/hacker/a`. It is inside my home directory. And before expansion the argument is equal to three characters as by using `~` we are shortening the path `/home/hacker` to only one character.

```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{khQzYoeeM4lXyZ04i4eBcpNNRyW.dNzM4QDLxITN0czW}
