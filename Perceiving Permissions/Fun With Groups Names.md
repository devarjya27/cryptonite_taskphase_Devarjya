# Fun With Groups Names
As per the challenge we need to find out which group we, the `hacker`, are in using the `id` command then change the group ownership of `/flag` to that particular group so that we can get access to it. Upon reading `/flag` now should give us the flag.

# My Solve
Firstly I invoked the `id` command to see which group I was in, which was found out to be `grp23375`. Now listing the permissions for `/flag` using `ls -l /flag` we can see that it is a part of the `root` group, so I changed it by invoking `chgrp grp23375 /flag` after which i simply read the file using `cat /flag` which returned the required flag.

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp23375) groups=1000(grp23375)
hacker@permissions~fun-with-groups-names:~$ ls -l /flag
-r--r----- 1 root root 58 Oct 13 10:03 /flag
hacker@permissions~fun-with-groups-names:~$ chgrp grp23375 /flag
hacker@permissions~fun-with-groups-names:~$ ls -l /flag
-r--r----- 1 root grp23375 58 Oct 13 10:03 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{4iIk3dGHfb0pnZ2a2is8HWR3sN3.dJzNyUDLxITN0czW}
