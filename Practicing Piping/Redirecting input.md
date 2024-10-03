# Redirecting input

In this challlenge we use `<` to redirect the input. As per the challenge we need to redirect `PWN` to `/challenge/run` and `PWN` must contain the value `COLLEGE`. We store `COLLEGE` in `PWN` through `echo COLLEGE > PWN` and then we redirect `PWN` to `/challenge/run` by `/challenge/run < PWN`.
```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{QYvgzqgtojAXuuOheEHAUfB0ZDE.dBzN1QDLxITN0czW}
