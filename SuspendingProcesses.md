#**Processes and Jobs**

##**Suspending Processes**

I ran _/challenge/run_, suspended it and later ran _/challenge/run_.

_hacker@processes-suspending-processes:~$ /challenge/run_

_I'll only give you the flag if there's already another copy of me running in_

_this terminal... Let's check!_

_UID PID PPID C STIME TTY TIME CMD_

_root 99 66 0 12:04 pts/0 00:00:00 bash /challenge/run_

_root 101 99 0 12:04 pts/0 00:00:00 ps -f_

_I don't see a second me!_

_To pass this level, you need to suspend me and launch me again! You can_

_background me with Ctrl-Z or, if you're not ready to do that for whatever_

_reason, just hit Enter and I'll exit!_

_^Z_

_\[1\]+ Stopped /challenge/run_

_hacker@processes-suspending-processes:~$ /challenge/run_

_I'll only give you the flag if there's already another copy of me running in_

_this terminal... Let's check!_

_UID PID PPID C STIME TTY TIME CMD_

_root 99 66 0 12:04 pts/0 00:00:00 bash /challenge/run_

_root 106 66 0 12:05 pts/0 00:00:00 bash /challenge/run_

_root 108 106 0 12:05 pts/0 00:00:00 ps -f_

_Yay, I found another version of me! Here is the flag:_

_pwn.college{MKV1W-G_pquTgb9TZzJ232oesMd.dVDN4QDL1cTN0czW}_
