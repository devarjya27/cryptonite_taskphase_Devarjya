# Backgrounding Processes
In the previous challenge we used the `fg` command to resume processes and put them in the foreground of our terminal but in this challenge we need to use the `bg` command to resume processes and keep them in the background of our terminal which means we can use the terminal for other commands. 

# My Solve
As per the challenge we need to run `/challenge/run` then suspend it, then resume it using `bg` then run it again so that there exists two compies of `/challenge/run` simultaneously. Firstly we run `/challenge/run` then suspend it by pressing `Ctrl+Z` then we have to use the `bg` command to resume the process and keep it in the background, then run `/challenge/run` again thus giving us our required flag.
```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S+   bash /challenge/run
root          84 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S    bash /challenge/run
root          92 S    sleep 6h
root          93 S+   bash /challenge/run
root          95 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{Iq7X4OMaEEC_LAKTQhgxEwbqQxP.ddDN4QDLxITN0czW}

