# Position thy self
The challenge asks us to use the `cd` command to change directories. It asks us to go ahead with `/challenge/run` which then will say we are not in the correct directory and show the correct filepath through which we can correctly execute the program. We then need to use the `cd` command to change directory to the correct one before rerunning the program.
```bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/aarch64-linux-gnu/include/gnu
hacker@paths~position-thy-self:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{kiqAtDqXMDXU4F1miuP83Ywrz8_.dZDN1QDLxITN0czW}
