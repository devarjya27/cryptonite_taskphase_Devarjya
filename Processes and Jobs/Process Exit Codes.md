# Process Exit Codes
Every program exits with an exit code, whether they run succesfully or not, and we can access those exit codes using `?`. `$?` helps us to read the value of the exit code. If a program runs succesfully then it returns 0 otherwise it will return a non-zero exit code.

# My Solve
As per the challenge we are asked to run `/challenge/get-code` then using `?` we need to acces its exit code. We can do that by `echo $?`, `$` reads the value of the exit code and `echo` prints that value in the terminal. After that we need to pass the exit code as an argument of `/challenge/submit-code` to get the flag.
```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo &?
[1] 85

ssh-entrypoint: a: command not found
[1]+  Done                    echo
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ $?
ssh-entrypoint: 102: command not found
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
255
hacker@processes~process-exit-codes:~$ /challenge/submit-code 255
CORRECT! Here is your flag:
pwn.college{cuuTjWjYXVzL_9xoGUPplGhQv3R.dljN4UDLxITN0czW}
