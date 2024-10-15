# Setting PATH
The `PATH` variable defines a list of directories where the shell looks for commands. If a command isn't found in the directories specified by the `PATH` variable then we can modify the `PATH` variable to include the direcotry where that command exists. As per the challenge we need to modify the `PATH` variable to the directory where `win` is located because `/chalenge/run` will try to execute `win` by its bare name. The directory where `win` is located is `/challenge/more_commands/`. 

# My Solve
Firstly I set the `PATH` variable to the directory where `win` is located by doing `PATH=/challenge/more_commands/` after which i simply ran `/challenge/run` to get the flag.
```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{kg8SkQTxoxSo9TyXeCl1AURgB6r.dVzNyUDLxITN0czW}
