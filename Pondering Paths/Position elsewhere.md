# Position elsewhere
As far as I understand we are doing the same thing we did for Position thy self, we are invoking `/challenge/run` which says that we are in the wrong directory and gives us the correct directory, we execute `cd` with the correct filepath and then we invoke the program.

```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/aarch64-linux-gnu/include/gnu
hacker@paths~position-elsewhere:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{YVv0xc55DWEY5yB8TMEb-_sV7Uw.ddDN1QDLxITN0czW}
