# Changing Permissions
In this challenge we need to make use of the `chmod` command which changes the mode of a particular file. When we view a file the dashes and characters in the beginning have a particular meaning, the first three characters being the permissions for the current user, the next three characters being the permissions of the owner group and the last three characters are the permissions for other users. For example, `rw-r--r--` would mean that the user has read and write permissions but no executable permission, the group owners would have read permissions and other users will also have read permissions. As per the challenge we need to make it so that we have the permission to read the `/flag` file.

# My Solve
Firstly I did `ls -l /flag` to view info of `/flag` here we can see that the owner is `root` and that there are no permissions for `other users` which is us in this case. Thus to change the permissions I did `chmod o+r /flag` which will give read permission to `other users`. After this simply doing `cat /flag` will give us our required flag.
```bash
hacker@permissions~changing-permissions:~$ ls -l /flag
-r-------- 1 root root 58 Oct 13 17:12 /flag
hacker@permissions~changing-permissions:~$ chmod o+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{EIufiEIL_YWlKr4yqtVaeSVf4JU.dNzNyUDLxITN0czW}
