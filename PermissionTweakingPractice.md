#**Perceiving Permissions**

##**Permission Tweaking Practice**

I tweaked the permission of _/challenge/pwn_ for 8 times and later tweaked the permission of _/flag_ to read it.

_hacker@permissions-permission-tweaking-practice:~$ /challenge/run_

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

_Needed permissions of "/challenge/pwn": rw-------_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\- the user doesn't have execute permissions_

_\- the group doesn't have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permission-tweaking-practice:~$ chmod go-rwx /challenge/pwn_

_You set the correct permissions!_

_Round 1 (of 8)!_

_Current permissions of "/challenge/pwn": rw-------_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\- the user doesn't have execute permissions_

_\- the group doesn't have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": rwx------_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permission-tweaking-practice:~$ chmod u+x /challenge/pwn_

_You set the correct permissions!_

_Round 2 (of 8)!_

_Current permissions of "/challenge/pwn": rwx------_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\- the world doesn't have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": rwx---rw-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permission-tweaking-practice:~$ chmod o+rw /challenge/pwn_

_You set the correct permissions!_

_Round 3 (of 8)!_

_Current permissions of "/challenge/pwn": rwx---rw-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": rwxr--rw-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permission-tweaking-practice:~$ chmod g+r /challenge/pwn_

_You set the correct permissions!_

_Round 4 (of 8)!_

_Current permissions of "/challenge/pwn": rwxr--rw-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\- the group doesn't have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": rwxrw-rw-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permission-tweaking-practice:~$ chmod g+w /challenge/pwn_

_You set the correct permissions!_

_Round 5 (of 8)!_

_Current permissions of "/challenge/pwn": rwxrw-rw-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\* the group does have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": rwx-w-rw-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permission-tweaking-practice:~$ chmod g-r /challenge/pwn_

_You set the correct permissions!_

_Round 6 (of 8)!_

_Current permissions of "/challenge/pwn": rwx-w-rw-_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\* the world does have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": rwx-w-r--_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permission-tweaking-practice:~$ chmod o-w /challenge/pwn_

_You set the correct permissions!_

_Round 7 (of 8)!_

_Current permissions of "/challenge/pwn": rwx-w-r--_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\- the group doesn't have execute permissions_

_\* the world does have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_Needed permissions of "/challenge/pwn": rwx-wxr--_

_\* the user does have read permissions_

_\* the user does have write permissions_

_\* the user does have execute permissions_

_\- the group doesn't have read permissions_

_\* the group does have write permissions_

_\* the group does have execute permissions_

_\* the world does have read permissions_

_\- the world doesn't have write permissions_

_\- the world doesn't have execute permissions_

_hacker@permissions-permission-tweaking-practice:~$ chmod g+x /challenge/pwn_

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

_hacker@permissions-permission-tweaking-practice:~$ chmod u+r /flag_

_hacker@permissions-permission-tweaking-practice:~$ cat /flag_

_pwn.college{M3HBP-xDApYi7-E6nZmNEV5dUAf.dBTM2QDL1cTN0czW}_
