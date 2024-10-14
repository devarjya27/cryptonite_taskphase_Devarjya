# Chaining with Semicolons
We can chain multiple commands using `;`. This is equivalent to pressing Enter after each command, but it allows us to write and execute them all at once. Each command runs independtly when chained together regardless of whether the previous one succeeds or fails. As per the challenge we need to chain the commands `/challenge/pwn` and `/challenge/college` using `;`.

# My Solve
To chain the commands we can simply type `/challenge/pwn ; /challenge/college`.
```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn ; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{wJCzXNN8SPGoDBI26uJs8BWDqHr.dVTN4QDLxITN0czW}

