# Starting Backgrounded Processes
Instead of running a program, then suspending it, then resuming it in the background, we can directly run a process in the background by appending `&`. for example `/challenge/run &` will make sure that `/challenge/run` runs in the background.

# My Solve
To run `/challenge/run` in the background we need to append it with `&`.
```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 82



hacker@processes~starting-backgrounded-processes:~$ Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{8dyZhaLAZDG8VFnV4iTEzB80XfH.dlDN4QDLxITN0czW}
