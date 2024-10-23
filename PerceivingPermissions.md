# Perceiving Permissions

## Changing File Ownership

I changed the ownership of _/flag_ from _root_ to _hacker_ using _chown_ command.

    hacker@permissions-changing-file-ownership:~$ chown hacker /flag
    hacker@permissions-changing-file-ownership:~$ cat /flag
    pwn.college{cn5SpmF2UVXxjH2OKVsAd1zd9Hp.dFTM2QDL1cTN0czW}


## Groups and File

I changed the group of /flag from root to hacker using chgrp command.

    hacker@permissions-groups-and-files:~$ chgrp hacker /flag
    hacker@permissions-groups-and-files:~$ cat /flag
    pwn.college{MQ9cb_Dj1ZX5mKVTNqox07BA8Em.dFzNyUDL1cTN0czW}

## Fun with Groups Names

I used id command to view the group and changed the group of /flag to grp20546 using chgrp command.

    hacker@permissions-fun-with-groups-names:~$ id
    uid=1000(hacker) gid=1000(grp20546) groups=1000(grp20546)
    hacker@permissions-fun-with-groups-names:~$ chgrp grp20546 /flag
    hacker@permissions-fun-with-groups-names:~$ cat /flag
    pwn.college{s8l9ij3jU21CdXKzn1nSg7P0RLb.dJzNyUDL1cTN0czW}

## Changing Permissions

I changed the permissions of /flag file using chmod (change mode) command.

    hacker@permissions-changing-permissions:~$ chmod 644 /flag
    hacker@permissions-changing-permissions:~$ cat /flag
    pwn.college{or6aRZuA9zevyPRxbp2pPYaJpTc.dNzNyUDL1cTN0czW}

## Executable Files

I made the /challenge/run program executable using chmod +x command and later ran /challenge/run.

    hacker@permissions-executable-files:~$ chmod +x /challenge/run
    hacker@permissions-executable-files:~$ /challenge/run
    Successful execution! Here is your flag:
    pwn.college{06rm7jwrS-kzC4vjE-oOEpIczaQ.dJTM2QDL1cTN0czW}

## Permission Tweaking Practice

I tweaked the permission of /challenge/pwn for 8 times and later tweaked the permission of /flag to read it.

    hacker@permissions-permission-tweaking-practice:~$ /challenge/run

    Round 0 (of 8)!

    Current permissions of "/challenge/pwn": rw-r--r--

    * the user does have read permissions

    * the user does have write permissions

    - the user doesn't have execute permissions

    * the group does have read permissions

    - the group doesn't have write permissions

    - the group doesn't have execute permissions

    * the world does have read permissions

    - the world doesn't have write permissions

    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rw-------
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    - the user doesn't have execute permissions
    
    - the group doesn't have read permissions
    
    - the group doesn't have write permissions

    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permission-tweaking-practice:~$ chmod go-rwx /challenge/pwn
    
    You set the correct permissions!
    
    Round 1 (of 8)!
    
    Current permissions of "/challenge/pwn": rw-------
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    - the user doesn't have execute permissions
    
    - the group doesn't have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rwx------
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permission-tweaking-practice:~$ chmod u+x /challenge/pwn
    
    You set the correct permissions!
    
    Round 2 (of 8)!
    
    Current permissions of "/challenge/pwn": rwx------
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rwx---rw-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permission-tweaking-practice:~$ chmod o+rw /challenge/pwn
    
    You set the correct permissions!
    
    Round 3 (of 8)!
    
    Current permissions of "/challenge/pwn": rwx---rw-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rwxr--rw-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permission-tweaking-practice:~$ chmod g+r /challenge/pwn
    
    You set the correct permissions!
    
    Round 4 (of 8)!
    
    Current permissions of "/challenge/pwn": rwxr--rw-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rwxrw-rw-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permission-tweaking-practice:~$ chmod g+w /challenge/pwn
    
    You set the correct permissions!
    
    Round 5 (of 8)!
    
    Current permissions of "/challenge/pwn": rwxrw-rw-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rwx-w-rw-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permission-tweaking-practice:~$ chmod g-r /challenge/pwn
    
    You set the correct permissions!
    
    Round 6 (of 8)!
    
    Current permissions of "/challenge/pwn": rwx-w-rw-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rwx-w-r--
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permission-tweaking-practice:~$ chmod o-w /challenge/pwn
    
    You set the correct permissions!
    
    Round 7 (of 8)!
    
    Current permissions of "/challenge/pwn": rwx-w-r--
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rwx-wxr--
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    * the group does have execute permissions
    
    * the world does have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permission-tweaking-practice:~$ chmod g+x /challenge/pwn
    
    You set the correct permissions!
    
    You've solved all 8 rounds! I have changed the ownership
    
    of the /flag file so that you can 'chmod' it. You won't be able to read
    
    it until you make it readable with chmod!
    
    Current permissions of "/flag": ---------
    
    - the user doesn't have read permissions
    
    - the user doesn't have write permissions
    
    - the user doesn't have execute permissions
    
    - the group doesn't have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permission-tweaking-practice:~$ chmod u+r /flag
    hacker@permissions-permission-tweaking-practice:~$ cat /flag
    pwn.college{M3HBP-xDApYi7-E6nZmNEV5dUAf.dBTM2QDL1cTN0czW}

## Permissions Setting Practice

I set the permission of /challenge/pwn for 8 times and later set the permission of /flag to read it.

    hacker@permissions-permissions-setting-practice:~$ /challenge/run
    Round 0 (of 8)!
    Current permissions of "/challenge/pwn": rw-r--r--
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    - the user doesn't have execute permissions
    
    * the group does have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rwxr---wx
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    * the world does have write permissions
    
    * the world does have execute permissions
    
    hacker@permissions-permissions-setting-practice:~$ chmod u=rwx,g=r,o=wx /challenge/pwn
    
    You set the correct permissions!
    
    Round 1 (of 8)!
    
    Current permissions of "/challenge/pwn": rwxr---wx
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    * the world does have write permissions
    
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": rwx-w--w-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permissions-setting-practice:~$ chmod u=rwx,g=w,o=w /challenge/pwn
    
    You set the correct permissions!
    
    Round 2 (of 8)!
    
    Current permissions of "/challenge/pwn": rwx-w--w-
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": r---wxr--
    
    * the user does have read permissions
    
    - the user doesn't have write permissions
    
    - the user doesn't have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    * the group does have execute permissions
    
    * the world does have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permissions-setting-practice:~$ chmod u=r,g=wx,o=r /challenge/pwn
    
    You set the correct permissions!
    
    Round 3 (of 8)!
    
    Current permissions of "/challenge/pwn": r---wxr--
    
    * the user does have read permissions
    
    - the user doesn't have write permissions
    
    - the user doesn't have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    * the group does have execute permissions
    
    * the world does have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": r-xrw---x
    
    * the user does have read permissions
    
    - the user doesn't have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    * the world does have execute permissions
    
    hacker@permissions-permissions-setting-practice:~$ chmod u=rx,g=rw,o=x /challenge/pwn
    
    You set the correct permissions!
    
    Round 4 (of 8)!
    
    Current permissions of "/challenge/pwn": r-xrw---x
    
    * the user does have read permissions
    
    - the user doesn't have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    * the group does have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": ---r-xrw-
    
    - the user doesn't have read permissions
    
    - the user doesn't have write permissions
    
    - the user doesn't have execute permissions
    
    * the group does have read permissions
    
    - the group doesn't have write permissions
    
    * the group does have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permissions-setting-practice:~$ chmod u=,g=rx,o=rw /challenge/pwn
    
    You set the correct permissions!
    
    Round 5 (of 8)!
    
    Current permissions of "/challenge/pwn": ---r-xrw-
    
    - the user doesn't have read permissions
    
    - the user doesn't have write permissions
    
    - the user doesn't have execute permissions
    
    * the group does have read permissions
    
    - the group doesn't have write permissions
    
    * the group does have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": rwxr--rwx
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    * the world does have execute permissions
    
    hacker@permissions-permissions-setting-practice:~$ chmod u=rwx,g=r,o=rwx /challenge/pwn
    
    You set the correct permissions!
    
    Round 6 (of 8)!
    
    Current permissions of "/challenge/pwn": rwxr--rwx
    
    * the user does have read permissions
    
    * the user does have write permissions
    
    * the user does have execute permissions
    
    * the group does have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    * the world does have read permissions
    
    * the world does have write permissions
    
    * the world does have execute permissions
    
    Needed permissions of "/challenge/pwn": -w--wx---
    
    - the user doesn't have read permissions
    
    * the user does have write permissions
    
    - the user doesn't have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    * the group does have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permissions-setting-practice:~$ chmod u=w,g=wx,o= /challenge/pwn
    
    You set the correct permissions!
    
    Round 7 (of 8)!
    
    Current permissions of "/challenge/pwn": -w--wx---
    
    - the user doesn't have read permissions
    
    * the user does have write permissions
    
    - the user doesn't have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    * the group does have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    Needed permissions of "/challenge/pwn": -w--wx-w-
    
    - the user doesn't have read permissions
    
    * the user does have write permissions
    
    - the user doesn't have execute permissions
    
    - the group doesn't have read permissions
    
    * the group does have write permissions
    
    * the group does have execute permissions
    
    - the world doesn't have read permissions
    
    * the world does have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permissions-setting-practice:~$ chmod u=w,g=wx,o=w /challenge/pwn
    
    You set the correct permissions!
    
    You've solved all 8 rounds! I have changed the ownership
    
    of the /flag file so that you can 'chmod' it. You won't be able to read
    
    it until you make it readable with chmod!
    
    Current permissions of "/flag": ---------
    
    - the user doesn't have read permissions
    
    - the user doesn't have write permissions
    
    - the user doesn't have execute permissions
    
    - the group doesn't have read permissions
    
    - the group doesn't have write permissions
    
    - the group doesn't have execute permissions
    
    - the world doesn't have read permissions
    
    - the world doesn't have write permissions
    
    - the world doesn't have execute permissions
    
    hacker@permissions-permissions-setting-practice:~$ chmod u=r,g=,o=r /flag
    hacker@permissions-permissions-setting-practice:~$ cat /flag
    pwn.college{chxUkyHayltjPMFOlNUwjzSNJkw.dNTM5QDL1cTN0czW}

## The SUID Bit

I added the SUID bit to the /challenge/getroot program using chmod u+s command to spawn a root shell to cat the flag.

    hacker@permissions-the-suid-bit:~$ chmod u+s /challenge/getroot
    hacker@permissions-the-suid-bit:~$ ls -l /challenge/getroot
    -rwsr-xr-x 1 root root 155 Jul 12 10:30 /challenge/getroot
    hacker@permissionsthe-suid-bit:$ /challenge/getroot
    SUCCESS! You have set the suid bit on this program, and it is running as root!
    Here is your shell...
    root@permissions-the-suid-bit:~# cat /flag
    pwn.college{gGOneiGVVmUuRe8wGqTcGM78m1i.dNTM2QDL1cTN0czW}



    
