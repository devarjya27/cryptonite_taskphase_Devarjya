# Adding Command
In this challenge we need to create a shell script called `win` which was provided to us in the last challenge but this time around we need to create it ourselves. `win` should display the ontents of `/flag` using `cat`. After making the shell script we need to make sure that the script is specified under the variable `PATH`. So we need to modify the `PATH` variable but we need to keep in mind that after modification of `PATH`, the `cat` command becomes inaccesible so we need to run `cat` in the shell script using its absolute path.

# My Solve
After struggling for a little while, I found out that we need to put in the absolute path of `cat` in our shell script. so to find out the absolute path of `cat` i did `which cat` which gave me the absolute path. After trying with this path i was not getting the solution so i did `ls -l` and found out that the absolute path is a symbolic link to `/run/dojo/bin/cat` so i went ahead with this path to be specified in the shell script. I made a directory called solution where i will store my shell script. I did `echo "/run/dojo/bin/cat" > /home/hacker/solution/win` which is essentially putting in `cat /flag` in `win`. Then i changed it mode to make it a executable by doing `chmod a+x win` which allowed all users to execute `win`. After that I modified the `PATH` variable to `/home/hacker/solution` which is the directory where `win` is stored. After that i simply did `/challenge/run` and got the required flag.
```bash
hacker@path~adding-commands:~$ which cat
/run/workspace/bin/cat
hacker@path~adding-commands:~$ ls -l /run/workspace/bin/cat
lrwxrwxrwx 1 root root 17 Jan  1  1970 /run/workspace/bin/cat -> /run/dojo/bin/cat
hacker@path~adding-commands:~$ mkdir solution
hacker@path~adding-commands:~$ cd solution
hacker@path~adding-commands:~/solution$ echo "/run/dojo/bin/cat" > /home/hacker/solution/win
hacker@path~adding-commands:~/solution$ ls -l /run/dojo/bin/cat
lrwxrwxrwx 16 root root 65 Jan  1  1970 /run/dojo/bin/cat -> /nix/store/k71apxkm38m3g34k01sb6zhysi0y7gph-coreutils-9.5/bin/cat
hacker@path~adding-commands:~/solution$ ls -l /run/dojo/bin/cat /flag
-r--------  1 root root 58 Oct 15 10:26 /flag
lrwxrwxrwx 16 root root 65 Jan  1  1970 /run/dojo/bin/cat -> /nix/store/k71apxkm38m3g34k01sb6zhysi0y7gph-coreutils-9.5/bin/cat
hacker@path~adding-commands:~/solution$ echo "/run/dojo/bin/cat /flag" > /home/hacker/solution/win
hacker@path~adding-commands:~/solution$ chmod a+x win
hacker@path~adding-commands:~/solution$ PATH=/home/hacker/solution
hacker@path~adding-commands:~/solution$ /challenge/run
Invoking 'win'....
pwn.college{kWfuac1YLxm9wKbInQRwST02HWV.dZzNyUDLxITN0czW}
