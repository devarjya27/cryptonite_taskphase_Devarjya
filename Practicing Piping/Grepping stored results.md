# Grepping stored results
In this challenge, in addition to the `>` command we need to use the `grep` command too. As per the challenge we need to redirect the output of `/challenge/run` to `/tmp/data.txt` which we do by `/challenge/run > /tmp.data.txt` after which we read the flag from `data.txt` by typing `grep "pwn.college" /tmp/data.txt` as we know the flag contains the string `pwn.college`.
```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep "pwn.college" /tmp/data.txt
pwn.college{Qp59TQPBGZcsjpQtlAMnvg55_3w.dhTM4QDLxITN0czW}
