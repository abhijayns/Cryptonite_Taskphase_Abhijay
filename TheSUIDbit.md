#**Perceiving Permissions**

##**The SUID Bit**

I added the SUID bit to the _/challenge/getroot_ program using _chmod u+s_ command to spawn a root shell to cat the flag.

_hacker@permissions-the-suid-bit:~$ chmod u+s /challenge/getroot_

_hacker@permissions-the-suid-bit:~$ ls -l /challenge/getroot_

_\-rwsr-xr-x 1 root root 155 Jul 12 10:30 /challenge/getroot_

_hacker@permissions~the-suid-bit:~$ /challenge/getroot_

_SUCCESS! You have set the suid bit on this program, and it is running as root!_

_Here is your shell..._

_root@permissions-the-suid-bit:~# cat /flag_

_pwn.college{gGOneiGVVmUuRe8wGqTcGM78m1i.dNTM2QDL1cTN0czW}_
