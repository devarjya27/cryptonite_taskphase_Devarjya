# implicit relative path

In this challenge we use the same concept of `.` which we used before. We execute `cd /challenge` to go our current working directory which, in this case, is `/challenge` and then we execute `./run` which means go to our current working directory and invoke `run` which is equivalent to `/challenge/run`.

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{IhdRAsLkUNZWFKrVyrqhbV4wVB3.dFTN1QDLxITN0czW}
