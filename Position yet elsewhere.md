# Position yet elsewhere
We are again doing the same thing as the last two challenges. This time the only difference that I see is that the directory in which the program is, is different. We execute `cd` with the correct filepath and then invoke the progam.

```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /usr/share/doc
hacker@paths~position-yet-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EmUdf7m9iLfzXykDbDe0tTli2GG.dhDN1QDLxITN0czW}
