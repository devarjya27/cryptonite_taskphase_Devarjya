# Becoming root with su
In this challenge we need to use the `su` command, which stands for switch user, to switch user to `root`. The `su` command allows users to elevate privileges to another user, typically root. It works because the `su` binary has the `SUID` bit set, allowing it to run with the permissions of `root`. As per the challenge we need to invooke the `su` command and type in `hack-the-planet` as the password to gain administrative priviledges which will allow us to read the flag.

# My Solve
Firstly we invooke `su` then type in `hack-the-planet` as its the password which gives us `root` permissions after which can simply read flag using the `cat` command.
```bash
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{UqBszR5uyUNxPt7a9WFE4oLHTVl.dVTN0UDLxITN0czW}
