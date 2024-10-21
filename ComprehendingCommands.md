#**Comprehending Commands**

## Cat command

I learnt to use _cat_ command to concatenate  

    hacker@commands-cat-not-the-pet-but-the-command:~/Desktop$ cd /
    hacker@commands-cat-not-the-pet-but-the-command:/$ cat flag
    pwn.college{UEpSbziv8VM78ZeMuHAFNEhf5C.dFzN1QDL1cTN0czW}


## Catting absolute paths

I learnt to read a file with cat and its absolute path /flag

    hacker@commands-catting-absolute-paths:~/Desktop$ cd /
    hacker@commands-catting-absolute-paths:/$ cat /flag


## Grepping for a needle in a haystack

Searched the flag in a file using grep command

    hacker@commands-grepping-for-a-needle-in-a-haystack:~/Desktop$ grep pwn.college /challenge/data.txt

## Listing Files

Listed the files and ran it

    hacker@commands-listing-files:~/Desktop$ ls /challenge
    3308-renamed-run-23729 DESCRIPTION.md
    hacker@commands-listing-files:~/Desktop$ /challenge/3308-renamed-run-23729 DESCRIPTION.md
    Yahaha, you found me!


## Touching Files

Created new blank files using touch command

    hacker@commands~touching-files:/$ cd /tmp
    hacker@commands~touching-files:/tmp$ touch pwn
    hacker@commands~touching-files:/tmp$ touch college
    hacker@commands~touching-files:/tmp$ /challenge/run
    Success!

## Removing Files

Created new blank files using touch command and removed it using rm command

    hacker@commands-removing-files:~/Desktop$ touch delete_me
    hacker@commands-removing-files:~/Desktop$ rm ~/delete_me
    hacker@commands-removing-files:~/Desktop$ /challenge/check
    Excellent removal.

## Hidden Files
    Found the hidden dot-prepended file using ls -a command
    hacker@commands-hidden-files:~/Desktop$ cd /
    hacker@commands~hidden-files:/$ ls -a
    . .dockerenv bin challenge etc lib lib64 media nix proc run srv tmp var
    .. .flag-6969276282698 boot dev home lib32 libx32 mnt opt root sbin sys usr
    hacker@commands~hidden-files:/$ grep pwn.college /.flag-6969276282698

## An epic file system quest

Followed the given instructions and applied the knowledge I gained in the challenges so far and found the flag.
I’m thankful to CRYPTONITE for making me do the challenges in pwn.college else I would have missed something so interesting, in my life. 

    hacker@commands-an-epic-filesystem-quest:/opt/angr-management/_internal/PySide6/Qt/qml/QtQuick/Layouts$ cd / hacker@commands-an-epic-filesystem-quest:/$ ls -a . .dockerenv bin challenge etc home lib32 libx32 mnt opt root sbin sys usr .. BRIEF boot dev flag lib lib64 media nix proc run srv tmp var hacker@commands-an-epic-filesystem-quest:/$ cat BRIEF Great sleuthing! The next clue is in: /usr/lib/x86_64-linux-gnu/libgtk-3-0

    The next clue is delayed --- it will not become readable until you enter the directory with 'cd'. hacker@commands-an-epic-filesystem-quest:/$ cd /usr/lib/x86_64-linux-gnu/libgtk-3-0 hacker@commands-an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/libgtk-3-0$ ls -a . .. WHISPER tk-query-immodules-3.0 hacker@commands-an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/libgtk-3-0$ cat WHISper cat: WHISper: No such file or directory hacker@commands-an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/libgtk-3-0$ cat WHISPER Great sleuthing! The next clue is in: /usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX

    The next clue is hidden --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'. hacker@commands-an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/libgtk-3-0$ cd /usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX hacker@commands-an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX$ ls -a . .. .NOTE POSIX.so hacker@commands-an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX$ cat .NOTE Tubular find! The next clue is in: /opt/linux/linux-5.4/drivers/phy/mscc hacker@commands-an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/POSIX$ cd /opt/linux/linux-5.4/drivers/phy/mscc hacker@commands-an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/phy/mscc$ ls -a . .. HINT Kconfig Makefile phy-ocelot-serdes.c hacker@commands-an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/phy/mscc$ cat HINT Great sleuthing! The next clue is in: /opt/aflplusplus/utils/asan_cgroups

    The next clue is hidden --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'. hacker@commands-an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/phy/mscc$ cd /opt/aflplusplus/utils/asan_cgroups hacker@commands-an-epic-filesystem-quest:/opt/aflplusplus/utils/asan_cgroups$ ls -a . .. .REVELATION limit_memory.sh hacker@commands-an-epic-filesystem-quest:/opt/aflplusplus/utils/asan_cgroups$ cat .REVELATION Yahaha, you found me! The next clue is in: /opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x

    The next clue is delayed --- it will not become readable until you enter the directory with 'cd'. hacker@commands-an-epic-filesystem-quest:/opt/aflplusplus/utils/asan_cgroups$ cd /opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x hacker@commands-an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x$ ls Makefile.target TIP csst.c exrl-trt.c exrl-trtr.c hello-s390x.c ipm.c mvc.c mvo.c pack.c hacker@commands-an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x$ cat TIP Yahaha, you found me! The next clue is in: /opt/angr-management/_internal/PySide6/Qt/qml/QtQuick/Layouts

    Watch out! The next clue is trapped. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct! hacker@commands-an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x$ ls /opt/angr-management/_internal/PySide6/Qt/qml/QtQuick/Layouts DISPATCH-TRAPPED libqquicklayoutsplugin.so plugins.qmltypes qmldir hacker@commands-an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x$ cat /opt/angr-management/_internal/PySide6/Qt/qml/QtQuick/Layouts/DISPATCH-TRAPPED Tubular find! The next clue is in: /opt/linux/linux-5.4/tools/perf/pmu-events/arch/x86/ivybridge hacker@commands-an-epic-filesystem-quest:/opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/s390x$ cd /opt/linux/linux-5.4/tools/perf/pmu-events/arch/x86/ivybridge hacker@commands-an-epic-filesystem-quest:/opt/linux/linux-5.4/tools/perf/pmu-events/arch/x86/ivybridge$ ls -a . README floating-point.json ivb-metrics.json other.json uncore.json .. cache.json frontend.json memory.json pipeline.json virtual-memory.json hacker@commands-an-epic-filesystem-quest:/opt/linux/linux-5.4/tools/perf/pmu-events/arch/x86/ivybridge$ cat README Yahaha, you found me! The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Arrows/Regular

    The next clue is delayed --- it will not become readable until you enter the directory with 'cd'. hacker@commands-an-epic-filesystem-quest:/opt/linux/linux-5.4/tools/perf/pmu-events/arch/x86/ivybridge$ cd /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Arrows/Regular hacker@commands-an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Arrows/Regular$ ls -a . .. Main.js NUGGET hacker@commands-an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Arrows/Regular$ cat NUGGET CONGRATULATIONS! Your perserverence has paid off, and you have found the flag! It is: pwn.college{EdhJjpL5Fzq1WyP2Wi0GKJvYR-Z.dljM4QDL1cTN0czW}

## Making Directories

Made a new directory /tmp/pwn using mkdir command and created a file named college using touch command.

    hacker@commands-making-directories:/tmp$ cd /tmp
    hacker@commands-making-directories:/tmp$ mkdir pwn
    hacker@commands-making-directories:/tmp$ cd /tmp/pwn
    hacker@commands-making-directories:/tmp/pwn$ touch college
    hacker@commands-making-directories:/tmp/pwn$ /challenge/run
    Success!

## Finding Files

Found the file named as flag in / directory using find command.

Syntax: find / -name <filename>

    hacker@commands~finding-files:/$ cd /
    hacker@commands~finding-files:/$ find / -name flag
    find: ‘/tmp/tmp.MiOQGWw5Zc’: Permission denied
    find: ‘/etc/ssl/private’: Permission denied
    /usr/local/lib/python3.8/dist-packages/pwnlib/flag
    /usr/local/share/afl/testcases/archives/common/gzip/flag
    pwn.college{0az8gwPEB3HUTG_BTWWgzikNpB1.dJzM4QDL1cTN0czW}

## Linking Files

A hard link is when you address your appartment using multiple addresses that all lead directly to the same place (e.g., Apt 2 vs Unit 2).
A soft link is when you move appartments and have the postal service automatically forward your mail from your old place to your new place.
A symbolic link (symlink) is created with the ln command with the -s argument

    hacker@commands~linking-files:/$ cd /
    hacker@commands~linking-files:/$ ln -s /flag /home/hacker/not-the-flag
    hacker@commands~linking-files:/$ /challenge/catflag
    About to read out the /home/hacker/not-the-flag file!
