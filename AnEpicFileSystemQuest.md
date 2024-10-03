#**Comprehending Commands**

##**An epic file system quest**

Followed the given instructions and applied the knowledge I gained in the challenges so far and found the flag.  
I’m thankful to CRYPTONITE for making me do the challenges in pwn.college else I would have missed something so interesting, in my life.
hacker@commands~an-epic-filesystem-quest:/opt/angr-management/_internal/PySide6/Qt/qml/QtQuick/Layouts$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.   .dockerenv  bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
..  BRIEF       boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@commands~an-epic-filesystem-quest:/$ cat BRIEF
Great sleuthing!
The next clue is in: /usr/lib/x86_64-linux-gnu/libgtk-3-0

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/lib/x86_64-linux-gnu/libgtk-3-0
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/libgtk-3-0$ ls -a
.  ..  WHISPER  gtk-query-immodules-3.0
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/libgtk-3-0$ cat WHISper
cat: WHISper: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/libgtk-3-0$ cat WHISPER
Great sleuthing!
The next clue is in: /usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/libgtk-3-0$ cd /usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX$ ls -a
.  ..  .NOTE  POSIX.so
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX$ cat .NOTE
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/phy/mscc
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX$ cd /opt/linux/linux-5.4/drivers/phy/mscc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/phy/mscc$ ls -a
.  ..  HINT  Kconfig  Makefile  phy-ocelot-serdes.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/phy/mscc$ cat HINT
Great sleuthing!
The next clue is in: /opt/aflplusplus/utils/asan_cgroups

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/phy/mscc$ cd /opt/aflplusplus/utils/asan_cgroups
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/utils/asan_cgroups$ ls -a
.  ..  .REVELATION  limit_memory.sh
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/utils/asan_cgroups$ cat .REVELATION
Yahaha, you found me!
The next clue is in: /opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/utils/asan_cgroups$ cd /opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x$ ls
Makefile.target  TIP  csst.c  exrl-trt.c  exrl-trtr.c  hello-s390x.c  ipm.c  mvc.c  mvo.c  pack.c
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x$ cat TIP
Yahaha, you found me!
The next clue is in: /opt/angr-management/_internal/PySide6/Qt/qml/QtQuick/Layouts

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!

_CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!_
