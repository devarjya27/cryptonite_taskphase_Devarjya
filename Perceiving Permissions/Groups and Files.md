# Groups and Files
In this challenge, we need to use the `chgrp` command to change the group of a particular file. We can check what groups the user currently is in using the `id` command. At times, instead of changing the ownership of a file to acces it we can change the group or becoma part of the group that has acces to the file. As per the challenge we need to change the group ownership of `/flag` to access it, this group is currently `root` but we need to change it to a group `hacker` is currently in so that we can access it and then read it to get the flag.

# My Solve
Firstly I invoked `ls -l /flag` to check the permissions of `/flag` and I found out that the current group which has ownership of `/flag` is root. Then i invoked `id` to check which group the user `hacker` is a part of. I am currently in the group `hacker` so changing the group ownership of `/flag` to `hacker` will allow us to access it. We change the group using `chgrp hacker/flag` then i listed the permissions of `/flag` again to confirm the group is indeed `hacker`. After that we simply read `/flag` to get the flag.
```bash
hacker@permissions~groups-and-files:~$ ls -l /flag
-r--r----- 1 root root 58 Oct 13 09:51 /flag
hacker@permissions~groups-and-files:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ ls -l /flag
-r--r----- 1 root hacker 58 Oct 13 09:51 /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{g2sn7C2XVqx5nbOHurOLRFcUzq9.dFzNyUDLxITN0czW}
