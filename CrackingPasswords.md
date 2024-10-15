#**Untangling Users**

##**Cracking Passwords**

I cracked the password using _john_ command and later switched user to zardus and ran _/challenge/run_.

_hacker@users-cracking-passwords:~$ john /challenge/shadow-leak_

_Loaded 1 password hash (crypt, generic crypt(3) \[?/64\])_

_Press 'q' or Ctrl-C to abort, almost any other key for status_

_0g 0:00:00:16 0% 2/3 0g/s 279.2p/s 279.2c/s 279.2C/s keller..nation_

_aardvark (zardus)_

_1g 0:00:00:20 100% 2/3 0.04798g/s 279.4p/s 279.4c/s 279.4C/s Johnson..buzz_

_Use the "--show" option to display all of the cracked passwords reliably_

_Session completed_

_hacker@users-cracking-passwords:~$ su zardus_

_Password: aardvark_

_zardus@users-cracking-passwords:/home/hacker$ /challenge/run_

_Congratulations, you have become Zardus! Here is your flag:_

_pwn.college{0QHpK8gjzKxxsrxVfj7iSBQJKMZ.ddTN0UDL1cTN0czW}_
