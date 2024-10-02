# listing files

In this challenge we are asked to use the `ls` commands which lists all the contents of a particular directory. We execute `ls /challenge` to list the contents of the challenge directory so that we can find the renamed run program and then we execute it to get our flag.

```bash
hacker@commands~listing-files:~$ ls /challenge
2457-renamed-run-16721  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/2457-renamed-run-16721
Yahaha, you found me! Here is your flag:
pwn.college{o9AMM20HP4A0eyM41r69ztliuXn.dhjM4QDLxITN0czW}
