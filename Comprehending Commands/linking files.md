# linking files

In this challenge we use the `ln -s` command to create a symbolic link. The challenge asks us to create a symbolic link of `/flag` to `/home/hacker/not-the-flag` as running `/challenge/catflag` will read `/home/hacker/not-the-flag` thus after linking, `/challenge/catflag` will read `/flag`.

```bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{4U2VCOgHnRPOvOsElJAW9VSkZFO.dlTM1UDLxITN0czW}
