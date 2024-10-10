#**Processes and Jobs**

##**Listing Processes**

I listed running processes using the _ps_ command and ran the renamed file containing the flag.

_hacker@processes-listing-processes:~$ ps -ef_

_UID PID PPID C STIME TTY TIME CMD_

_root 1 0 0 13:33 ? 00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /ru_

_root 7 1 0 13:33 ? 00:00:00 /run/dojo/bin/sleep 6h_

_root 68 1 0 13:33 ? 00:00:00 /challenge/13771-run-12707_

_root 72 68 0 13:33 ? 00:00:00 sleep 6h_

_hacker 73 0 0 13:33 pts/0 00:00:00 /run/dojo/bin/ssh-entrypoint_

_hacker 90 73 0 13:33 pts/0 00:00:00 ps -ef_

_hacker@processes-listing-processes:~$ ps aux_

_USER PID %CPU %MEM VSZ RSS TTY STAT START TIME COMMAND_

_root 1 0.1 0.0 1056 640 ? Ss 13:33 0:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bi_

_root 7 0.0 0.0 5052 2240 ? S 13:33 0:00 /run/dojo/bin/sleep 6h_

_root 68 0.0 0.0 4132 2560 ? S 13:33 0:00 /challenge/13771-run-12707_

_root 72 0.0 0.0 2744 1280 ? S 13:33 0:00 sleep 6h_

_hacker 73 0.1 0.0 5372 3840 pts/0 Ss 13:33 0:00 /run/dojo/bin/ssh-entrypoint_

_hacker 91 0.0 0.0 7868 3520 pts/0 R+ 13:33 0:00 ps aux_

_hacker@processes-listing-processes:~$ /challenge/13771-run-12707_

_Yahaha, you found me! Here is your flag:_

_pwn.college{ELyM1XAQ7GBBBQ4ws84MUkpnKvq.dhzM4QDL1cTN0czW}_

_Now I will sleep for a while (so that you could find me with 'ps')._
