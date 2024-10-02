# more catting practice

In this challenge the flag file is stored in some random directory and we are also not allowed to use `cd` to change directories. The filepath is given to me as `/usr/sbin/flag`. Therefore we provide this absolute path as an argument for `cat`.

```bash
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /usr/sbin/flag. Go cat it out **without** cding into that directory!
hacker@commands~more-catting-practice:~$ cat /usr/sbin/flag
pwn.college{wvxZRL9jkgBhmlIfXRwLj9kUY3N.dBjM5QDLxITN0czW}
