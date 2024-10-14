# Other users with su
In this challenge we need to pass in a username as the argument for `su` to switch to that particular user. Without providing any argument the `su` command allows us to switch to the `root` user. As per the challenge we need to switch to the user named Zardus whose password is `dont-hack-me` and after switching we need to run `/challenge/run` to get the flag.

# My Solve
Firstly I passed in `zardus` as the argument for `su` after which i typed in the password which was `dont-hack-me` which allowed me to switch the user to zardus. After that simply invoking `/challenge/run` gave me the flag.
```bash
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{kI7s3lJsU1SUn9OjKQVR0CrMj6k.dZTN0UDLxITN0czW}

