# Cracking passwords
In this challenge we are asked to crack the password for the user `zardus`. Passwords are stored in `/etc/shadow` because it is not readable by regular users, unlike `/etc/passwd`, which is globally readable. The password field in `/etc/shadow` contains hashed passwords which are one way encrypted and if we obtain this hashed password due to any leaks of `/etc/shadow` we can crack the password easily.  When a user inputs a password the system hashes the inputted password using a one-way encryption method. It then compares the result to the corresponding hash stored in `/etc/shadow`. If the two hashes match, access is granted. If someone gets a hold of `/etc/shadow` through backup leaks etc they can attempt to crack the hashed passwords using tools like `John the Ripper Password Cracker`.

# My Solve
Firstly i did `john /challenge/shadow-leak` which will crack the passwords stored in `/challenge/shadow-leak`. We can see that the password for `zardus` is `aardvark` so now we do `su zardus` and put in `aardvark` as the password to get administrative priviledges. After that we simply run `/challenge/run` to get the flag.
```bash
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:21 100% 2/3 0.04621g/s 269.0p/s 269.0c/s 269.0C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{4Wui-dQvifzCYadocmjQy-HG97G.ddTN0UDLxITN0czW}
