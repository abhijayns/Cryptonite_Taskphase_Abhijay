#**Perceiving Permissions**

##**Permissions Setting Practice**

I set the permission of _/challenge/pwn_ for 8 times and later set the permission of _/flag_ to read it.

_hacker@permissions-permissions-setting-practice:~$ /challenge/run_

_Round 0 (of 8)!_

_Current permissions of "/challenge/pwn": rw-r--r--_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\- the user doesn't have execute permissions_

_\* the group does have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": rwxr---wx_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\* the world does have write permissions_

_\* the world does have execute permissions_

_hacker@permissions-permissions-setting-practice:~$ chmod u=rwx,g=r,o=wx /challenge/pwn_

_You set the correct permissions!_

_Round 1 (of 8)!_

_Current permissions of "/challenge/pwn": rwxr---wx_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\* the world does have write permissions_

_\* the world does have execute permissions_

_Needed permissions of "/challenge/pwn": rwx-w--w-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permissions-setting-practice:~$ chmod u=rwx,g=w,o=w /challenge/pwn_

_You set the correct permissions!_

_Round 2 (of 8)!_

_Current permissions of "/challenge/pwn": rwx-w--w-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": r---wxr--_

_\* the user does have read permissions_

_\- the user doesn't have write permissions_

_\- the user doesn't have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\* the group does have execute permissions_

_\* the world does have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permissions-setting-practice:~$ chmod u=r,g=wx,o=r /challenge/pwn_

_You set the correct permissions!_

_Round 3 (of 8)!_

_Current permissions of "/challenge/pwn": r---wxr--_

_\* the user does have read permissions_

_\- the user doesn't have write permissions_

_\- the user doesn't have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\* the group does have execute permissions_

_\* the world does have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": r-xrw---x_

_\* the user does have read permissions_

_\- the user doesn't have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\- the world doesn't have write permissions_

_\* the world does have execute permissions_

_hacker@permissions-permissions-setting-practice:~$ chmod u=rx,g=rw,o=x /challenge/pwn_

_You set the correct permissions!_

_Round 4 (of 8)!_

_Current permissions of "/challenge/pwn": r-xrw---x_

_\* the user does have read permissions_

_\- the user doesn't have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\- the world doesn't have write permissions_

_\* the world does have execute permissions_

_Needed permissions of "/challenge/pwn": ---r-xrw-_

_\- the user doesn't have read permissions_

_\- the user doesn't have write permissions_

_\- the user doesn't have execute permissions_

_\* the group does have read permissions_

_\- the group doesn't have write permissions_

_\* the group does have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permissions-setting-practice:~$ chmod u=,g=rx,o=rw /challenge/pwn_

_You set the correct permissions!_

_Round 5 (of 8)!_

_Current permissions of "/challenge/pwn": ---r-xrw-_

_\- the user doesn't have read permissions_

_\- the user doesn't have write permissions_

_\- the user doesn't have execute permissions_

_\* the group does have read permissions_

_\- the group doesn't have write permissions_

_\* the group does have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": rwxr--rwx_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\* the world does have execute permissions_

_hacker@permissions-permissions-setting-practice:~$ chmod u=rwx,g=r,o=rwx /challenge/pwn_

_You set the correct permissions!_

_Round 6 (of 8)!_

_Current permissions of "/challenge/pwn": rwxr--rwx_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\* the world does have execute permissions_

_Needed permissions of "/challenge/pwn": -w--wx---_

_\- the user doesn't have read permissions_

_\* the user does have write permissions_

_\- the user doesn't have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\* the group does have execute permissions_

_\- the world doesn't have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permissions-setting-practice:~$ chmod u=w,g=wx,o= /challenge/pwn_

_You set the correct permissions!_

_Round 7 (of 8)!_

_Current permissions of "/challenge/pwn": -w--wx---_

_\- the user doesn't have read permissions_

_\* the user does have write permissions_

_\- the user doesn't have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\* the group does have execute permissions_

_\- the world doesn't have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": -w--wx-w-_

_\- the user doesn't have read permissions_

_\* the user does have write permissions_

_\- the user doesn't have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\* the group does have execute permissions_

_\- the world doesn't have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permissions-setting-practice:~$ chmod u=w,g=wx,o=w /challenge/pwn_

_You set the correct permissions!_

_You've solved all 8 rounds! I have changed the ownership_

_of the /flag file so that you can 'chmod' it. You won't be able to read_

_it until you make it readable with chmod!_

_Current permissions of "/flag": ---------_

_\- the user doesn't have read permissions_

_\- the user doesn't have write permissions_

_\- the user doesn't have execute permissions_

_\- the group doesn't have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permissions-setting-practice:~$ chmod u=r,g=,o=r /flag_

_hacker@permissions-permissions-setting-practice:~$ cat /flag_

_pwn.college{chxUkyHayltjPMFOlNUwjzSNJkw.dNTM5QDL1cTN0czW}_
