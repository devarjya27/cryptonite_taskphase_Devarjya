# Listing Processes
In this challenge we need to use the `ps` command followed by certain arguments to list all the processes currently running. the `-ef` argument lists every process in a "full format" output. Whereas the `aux` argument outputs all the proccesses not running in the terminal for all users in a "user-readable" format. There are certain columns which are similar to `-ef` and `aux` like the `USER` column, the `PID` column, the `TTY` column, etc. There are also things which differ for example `-ef` additionally outputs the `PPID`, which is the `PID` of the process that launched the one in question, while `aux` outputs the percentage of total system CPU and Memory that the process is utilizing.

# My Solve
As per the challenge, the `/challenge/run` file has been renamed to a random name and we need to find that file by listing all the processes. We can do that by two ways, both `ps -ef` and `ps aux` have been shown in my solve. After finding the file, we simply run it to get the flag.
```bash
hacker@processes~listing-processes:/challenge$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   14:09   0:00 /sbin/docker-init -- /nix/var/nix/p
root           7  0.0  0.0   5052  2560 ?        S    14:09   0:00 /run/dojo/bin/sleep 6h
root          68  0.0  0.0   4132  2560 ?        S    14:09   0:00 /challenge/21633-run-6824
root          72  0.0  0.0   2744  1280 ?        S    14:09   0:00 sleep 6h
hacker        73  0.0  0.0   5372  3840 pts/0    Ss   14:09   0:00 /run/dojo/bin/ssh-entrypoint
hacker        99  0.0  0.0   7868  3200 pts/0    R+   14:11   0:00 ps aux
hacker@processes~listing-processes:/challenge$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 14:09 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default
root           7       1  0 14:09 ?        00:00:00 /run/dojo/bin/sleep 6h
root          68       1  0 14:09 ?        00:00:00 /challenge/21633-run-6824
root          72      68  0 14:09 ?        00:00:00 sleep 6h
hacker        73       0  0 14:09 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker       100      73  0 14:12 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:/challenge$ /challenge/21633-run-6824
Yahaha, you found me! Here is your flag:
pwn.college{0_yyegLbezPOeML0Obn9izKXChq.dhzM4QDLxITN0czW}
Now I will sleep for a while (so that you could find me with 'ps').
