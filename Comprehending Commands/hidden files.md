# hidden files

In this challenge we are asked to find the flag which is located in a hidden file. hidden files are files which are prepended by `.`. We execute `ls -a` to list all the files of a directory including the hidden files, then we view the hidden file's contents through the `cat` command.

```bash
hacker@commands~hidden-files:~$ ls /
bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv          bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-141166465714  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-141166465714
pwn.college{kOgOUUSiFGY4lUK6pPijChNjfDQ.dBTN4QDLxITN0czW}
