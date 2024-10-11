#**Processes and Jobs**

##**Killing Processes**

I found the _dont_run_ process and killed it using kill command and later ran _/challenge/run_ to get the flag.

_hacker@processes-killing-processes:~$ ps -ef | grep dont_run_

_hacker 73 71 0 17:16 ? 00:00:00 /challenge/dont_run_

_hacker 112 75 0 17:17 pts/1 00:00:00 grep --color=auto dont_run_

_hacker@processes-killing-processes:~$ kill 73_

_hacker@processes-killing-processes:~$ /challenge/run_

_Great job! Here is your payment:_

_pwn.college{0B4fRJS4NtX6FzGhxB16khq4Vlp.dJDN4QDL1cTN0czW}_
