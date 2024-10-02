# making directories

In this challenge we are asked to create `/tmp/pwn` directory and make a 'college' file in it. We use the `mkdir` command to make the directory then use the `touch` command to create the file.

```bash
hacker@commands~making-directories:~$ ls /
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  tmp.MiOQGWw5Zc
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{oVPpVciH1AuF6r3YN0D5wSfj6CL.dFzM4QDLxITN0czW}
