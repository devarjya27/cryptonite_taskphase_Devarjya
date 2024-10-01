# Explicit relative paths, from /

In this challenge we use `.` which refers to the current directory we are in. Thus `/challenge/.` is the same as `/challenge`. For the challenge we do `cd /` to go `/` which is our  current working directory and then we execute `./challenge/run` which means go to our current directory which is `/` and invoke `/challene/run`

```bash
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{siUlOGpybd7VrLdXj_CRo7IpBqt.dBTN1QDLxITN0czW}
