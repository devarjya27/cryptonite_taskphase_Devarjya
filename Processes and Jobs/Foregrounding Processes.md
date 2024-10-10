# Foregrounding Processes
In this challenge we need to put an already running process which is in the background in the foreground of our terminal using `fg`.

# My Solve
Firstly we need to run `/challenge/run` then we have to suspend it by pressing `Ctrl+Z`.After suspending it we need to resume it and put it in the background using `bg` then using the `fg` command, bring it back to the foreground of our terminal.
```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.
hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{Q9lIoNpjo3VNoYoWpTue5bIvrYl.dhDN4QDLxITN0czW}
