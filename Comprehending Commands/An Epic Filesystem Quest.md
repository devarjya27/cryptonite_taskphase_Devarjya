# An Epic Filesystem Quest

In this challenge, we need to use the commands that we have learned like `cat`,`cd`,`ls`,etc to find the flag. All I did was look for the clues in the directories and follow them until I got the flag.
```bash
hacker@commands~an-epic-filesystem-quest:~$ ls /
TEASER  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin     challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ cat flag
cat: flag: Permission denied
hacker@commands~an-epic-filesystem-quest:/$ cat TEASER
Congratulations, you found the clue!
The next clue is in: /opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern
hacker@commands~an-epic-filesystem-quest:/opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern$ ls
DOSSIER  __init__.py  __pycache__
hacker@commands~an-epic-filesystem-quest:/opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern$ ls -a
.  ..  DOSSIER  __init__.py  __pycache__
hacker@commands~an-epic-filesystem-quest:/opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern$ cat DOSSIER
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/include/config/randomize

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern$ cat /opt/linux/linux-5.4/include/config/randomize
cat: /opt/linux/linux-5.4/include/config/randomize: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern$ ls /opt/linux/linux-5.4/include/config/randomize
ALERT-TRAPPED  base.h  memory  memory.h
hacker@commands~an-epic-filesystem-quest:/opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern$ cat /opt/linux/linux-5.4/include/config/randomize/ALERT-TRAPPED
Lucky listing!
The next clue is in: /opt/radare2/test/db/formats
hacker@commands~an-epic-filesystem-quest:/opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern$ ls /opt/radare2/test/db/formats
CUE  bflt  coff  dmp  dwarf  firmware  gbc   java  mach0     mdmp    msil  mz  nes    nro  omf  pe      plan9  psx  qnx  smd  spc700   vsf           xbe    xcoff64  z64   zip
ar   cgc   dex   dol  elf    gba       hunk  le    mangling  menuet  msx   ne  ninds  nso  pdb  pebble  prg    pyc  rel  sms  symbols  web_assembly  xcoff  xtac     zimg
hacker@commands~an-epic-filesystem-quest:/opt/pwndbg/.venv/lib/python3.8/site-packages/setuptools/extern$ cd /opt/radare2/test/db/formats
hacker@commands~an-epic-filesystem-quest:/opt/radare2/test/db/formats$ ls -a
.   CUE  bflt  coff  dmp  dwarf  firmware  gbc   java  mach0     mdmp    msil  mz  nes    nro  omf  pe      plan9  psx  qnx  smd  spc700   vsf           xbe    xcoff64  z64   zip
..  ar   cgc   dex   dol  elf    gba       hunk  le    mangling  menuet  msx   ne  ninds  nso  pdb  pebble  prg    pyc  rel  sms  symbols  web_assembly  xcoff  xtac     zimg
hacker@commands~an-epic-filesystem-quest:/opt/radare2/test/db/formats$ cat CUE
Congratulations, you found the clue!
The next clue is in: /etc/kernel/install.d

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/radare2/test/db/formats$ cd /etc/kernel/install.d
hacker@commands~an-epic-filesystem-quest:/etc/kernel/install.d$ ls -a
.  ..  SPOILER
hacker@commands~an-epic-filesystem-quest:/etc/kernel/install.d$ cat SPOLIER
cat: SPOLIER: No such file or directory
hacker@commands~an-epic-filesystem-quest:/etc/kernel/install.d$ cat SPOILER
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/fs/lockd

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/etc/kernel/install.d$ cd /opt/linux/linux-5.4/fs/lockd
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/fs/lockd$ ls -a
.                .clnt4xdr.o.cmd  .host.o.cmd    .svc4proc.o.cmd  .svcsubs.o.cmd  built-in.a  clntlock.o  clntxdr.o  mon.o     procfs.o    svc4proc.o  svcproc.o   svcsubs.o  xdr4.o
..               .clntlock.o.cmd  .mon.o.cmd     .svclock.o.cmd   .xdr.o.cmd      clnt4xdr.c  clntproc.c  host.c     netns.h   svc.c       svclock.c   svcshare.c  xdr.c
.POINTER         .clntproc.o.cmd  .procfs.o.cmd  .svcproc.o.cmd   .xdr4.o.cmd     clnt4xdr.o  clntproc.o  host.o     procfs.c  svc.o       svclock.o   svcshare.o  xdr.o
.built-in.a.cmd  .clntxdr.o.cmd   .svc.o.cmd     .svcshare.o.cmd  Makefile        clntlock.c  clntxdr.c   mon.c      procfs.h  svc4proc.c  svcproc.c   svcsubs.c   xdr4.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/fs/lockd$ cat POINTER
cat: POINTER: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/fs/lockd$ cat .POINTER
Yahaha, you found me!
The next clue is in: /usr/share/maxima-sage/5.42.2/share/diff_form/tests

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/fs/lockd$ ls /usr/share/maxima-sage/5.42.2/share/diff_form/tests
NOTE-TRAPPED  rtest_diff_form.mac
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/fs/lockd$ cat /usr/share/maxima-sage/5.42.2/share/diff_form/tests/NOTE-TRAPPED
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/macintosh

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/fs/lockd$ cd /opt/linux/linux-5.4/drivers/macintosh
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/macintosh$ ls -a
.                Makefile   ans-lcd.h    macio_asic.c     therm_windtunnel.c   via-pmu-led.c             windfarm_fcu_controls.c    windfarm_pid.h    windfarm_rm31.c
..               adb-iop.c  apm_emu.c    macio_sysfs.c    via-cuda.c           via-pmu.c                 windfarm_lm75_sensor.c     windfarm_pm112.c  windfarm_smu_controls.c
.BRIEF           adb.c      built-in.a   mediabay.c       via-macii.c          windfarm.h                windfarm_lm87_sensor.c     windfarm_pm121.c  windfarm_smu_sat.c
.built-in.a.cmd  adbhid.c   mac_hid.c    rack-meter.c     via-pmu-backlight.c  windfarm_ad7417_sensor.c  windfarm_max6690_sensor.c  windfarm_pm72.c   windfarm_smu_sensors.c
.mac_hid.o.cmd   ams        mac_hid.o    smu.c            via-pmu-event.c      windfarm_core.c           windfarm_mpu.h             windfarm_pm81.c
Kconfig          ans-lcd.c  macio-adb.c  therm_adt746x.c  via-pmu-event.h      windfarm_cpufreq_clamp.c  windfarm_pid.c             windfarm_pm91.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/macintosh$ cat .BRIEF
Yahaha, you found me!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Shapes/BoldItalic

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/macintosh$ ls /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Shapes/BoldItalic
MESSAGE-TRAPPED  Main.js
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/macintosh$ cat /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Shapes/BoldItalic/MESSAGE-TRAPPED
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{41aDwPje6sQ1AXXXqGTYNeiAtvX.dljM4QDLxITN0czW}
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/macintosh$
