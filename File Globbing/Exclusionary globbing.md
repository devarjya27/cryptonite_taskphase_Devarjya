# Exclusionary globbing

In this challenge instead of searching for files with certain characters, we searching for files without certain characters. As per the challenge, we need to search for files that dont start with p,w, or n.


```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{c4OygdUV_APP1l4V3-DTFoiZEW0.dZjM4QDLxITN0czW}
hacker@globbing~exclusionary-globbing:/challenge/files$
