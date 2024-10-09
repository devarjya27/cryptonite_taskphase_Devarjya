# Storing Command Output
In this challenge we need to store the output of `/challenge/run` in the variable `PWN` and then print the variable to get the flag. We store the output of `/challenge/run` in `PWN` by doing `PWN=$(/challenge/run)` then using the `echo` command we can print `PWN`.

# My Solve
```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{UGrrcnMuqoyElfXDG99tSxFcTB0.dVzN0UDLxITN0czW}
