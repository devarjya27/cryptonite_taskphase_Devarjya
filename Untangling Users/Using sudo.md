# Using sudo
In this challenge we need to use the `sudo` command that allows users to run specific commands with elevated priviledges without needing to log in as the root or know the root password. Unlike `su`, which switches the user to a root shell, `sudo` runs individual commands as root.

# My Solve 
As per the challenge we need to read the flag which requires root permissions, thus we need to use `sudo` to give us the root permission to execute `cat /flag`.
```bash
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{YJbEwd4LcLU3cfKcGn96H1sh3cK.dhTN0UDLxITN0czW}
