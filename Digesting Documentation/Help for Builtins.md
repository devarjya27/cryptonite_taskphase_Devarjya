# Help for Builtins.md

In this challenge we use `help` that provides information on a particular builtin. it is said that `challenge` is a builtin thus executing `help challenge` will provide us with valuable info. After executing `help` we get the argument that returns the required flag.

```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "oCCuNZgx".
hacker@man~help-for-builtins:~$ challenge --fortune
Some rise by sin and some by virtue fall.
hacker@man~help-for-builtins:~$ challenge --secret oCCuNZgx
Correct! Here is your flag!
pwn.college{oCCuNZgxeJkU3IcA0ublFrdJVV8.dRTM5QDLxITN0czW}
