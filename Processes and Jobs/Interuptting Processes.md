# Interuptting Processes
`Ctrl+C` interrupts the application waiting for input at the terminal and cleanly exits that application.

# My Solve
As per the challenge we need to run the `/challenge/run` file then press `Ctrl+C` to interrupt it ang then we should get our flag.
```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{8hNG32W0h3Y7LJLg7lGl5I0DnmU.dNDN4QDLxITN0czW}
