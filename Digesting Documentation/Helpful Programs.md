# Helpful Programs

In this challenge we pass `--help` as the argument for `/challenge/challenge` to find which argument gives us the required flag, after executing `--help` we see that we need to use 2 different arguments to end up with the flag.
```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge --fortune
"Why can't we ever attempt to solve a problem in this country without having
a 'War' on it?" -- Rich Thomson, talk.politics.misc
hacker@man~helpful-programs:~$ /challenge/challenge --print-value
The secret value is: 944
hacker@man~helpful-programs:~$ /challenge/challenge -g 944
Correct usage! Your flag: pwn.college{opdBbt-pX9zadxr4NrfxfvQuAvN.ddjM4QDLxITN0czW}
