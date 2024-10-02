# Searching Manuals

In this challenge, we use the `man` command to get the manual for `challenge` after which we need to search for the argument that gives us the required flag. Although not showing up in the bash below as i pressed `q` to quit the manual, once the `man` command is executed I used the `/` command followed by `flag` to search for the argument that will give us the flag. The manual said that `--ge will give the required flag`. Thus passing `--ge` as the argument for `/challenge/challenge` we get our flag.

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --ge
Initializing...
Correct usage! Your flag: pwn.college{kOAzHYsvjCOABE4HrcbQjOvgP9r.dVTM4QDLxITN0czW}
