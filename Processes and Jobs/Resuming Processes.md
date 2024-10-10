# Resuming Processes
In this challenge we need to use the `fg` command to resume any suspended processes and put them back in the foreground of our terminal.

# My Solve
As per the challenge we need to suspend and then resume `/challenge/run`. We can do that by firstly running `/challenge/run` then press `Ctrl+Z` to suspend the process then execute the `fg` command that resumes it puts it back in the foreground.
```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{cVNrGBMH1MURP0Te4nPUsh6wcLP.dZDN4QDLxITN0czW}
