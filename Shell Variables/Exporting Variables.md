# Exporting Variables
In this challenge, we export the variable `PWN` set to the value `COLLEGE` and DON'T export the variable `COLLEGE` which is set to the value `PWN`. We can export using the `export` command. After that we invoke `/challenge/run` to get the flag.

# My Solve
```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{wvFt3y3jGsn6_5MD2FhPZ2fcPGK.dJjN1QDLxITN0czW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
