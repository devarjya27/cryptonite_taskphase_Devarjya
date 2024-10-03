# Split-piping stderr and stdout
In this challlenge we need to use the commands `>()`, `2>` and `|` to get our flag. As per the challenge we need to redirect the `stderr` of `/challenge/hack` to `/challenge/the` and the `stdout` to `/challenge/pplanet`. We can do this in a single command line as folllows:
```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) > >(/challenge/planet)
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{k3s7FGpGGrMEfkTxw0claFGh3mG.dFDNwYDLxITN0czW}
```
Again, this took me so many tries and fried my brain completely :(
