# Your First Shell Script
When we need to combine multiple complex commands the length of the combined prompt becomes very difficult to deal with it, so instead we can store those commands in a `shell script` and we can run that shell script by passing it as an argument to a new instance of our shell. As per the challenge we need to create a shell script containing two commands `/challenge/pwn` and `/challenge/college` and then running that particular shell script which is named as `x.sh` we can get the flag.

# My Solve
Firstly I did `echo /challenge/pwn > x.sh` which stores `/challenge/pwn` in `x.sh` then we append `x.sh` with `/challenge/college` by doing `echo /challenge/college >> x.sh`. This completes our shell script after which we simply run the shell script by doing `bash x.sh` which returns our required flag. 
```bash
hacker@chaining~your-first-shell-script:~$ echo /challenge/pwn > x.sh
hacker@chaining~your-first-shell-script:~$ echo /challenge/college >> x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{4dP00HFepl-w3vG5emnRh8CjO_t.dFzN4QDLxITN0czW}
