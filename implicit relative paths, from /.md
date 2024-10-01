# Implicit relative paths, from /
In the past 3 challenges, we are changing the directory by putting the absolute paths. In this challenge, we use the concept of relative paths. Th challenge says that our current working directory is `/` thus we need to execute `cd /` to go to our current working directory. The challenge then says that our relative path begins from the letter 'c' which clearly means the relative path starts from 'challenge' and by looking at the examples provided we can figure out that the relative path is `challenge/run` thus making our complete filepath `/challenge/run`

```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{Q9kW4VfqKSoL6_6QeotaG6HKVDc.dlDN1QDLxITN0czW}

