# Killing Processes
In this challenge, we need to use the `kill` command to terminate processes. We can terminate a process by first identifying its `PID` by listing the processes using `ps` then executing `kill <PID>`.

# My Solve
As per the challenge we need to run the `/challenge/run` file but we cannot do so until and unless we terminate the `/challenge/dont_run` process. Firstly we list the processes and look for the `PID` of the `/challenge/dont_run` file. We can see that it is `73` thus executing `kill 73` will terminate it. After that we simply run the `/challenge/run` file to get our flag.
```bash
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 14:27 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default
root           7       1  0 14:27 ?        00:00:00 /run/dojo/bin/sleep 6h
root          71       1  0 14:27 ?        00:00:00 su -c /challenge/.launcher hacker
hacker        73      71  0 14:27 ?        00:00:00 /challenge/dont_run
hacker        74      73  0 14:27 ?        00:00:00 sleep 6h
hacker        75       0  0 14:27 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker        93      75  0 14:27 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 73
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{YrSJQ4vNWH7K-2cNqZ-fFe0hTkv.dJDN4QDLxITN0czW}
