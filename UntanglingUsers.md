# Untangling Users

## Becoming root with su

I provided the password to the _su_ (switch user) command and read the flag.

    hacker@users-becoming-root-with-su:~$ su
    Password: hack-the-planet
    root@users-becoming-root-with-su:/home/hacker# cat /flag
    pwn.college{wqSct8Eq2zJ5agjAn97ieJklf16.dVTN0UDL1cTN0czW}
## Other users with su

I provided the password to the su (switch user) command to switch to zardus and ran /challenge/run.

    hacker@users-other-users-with-su:~$ su zardus
    Password: dont-hack-me
    zardus@users-other-users-with-su:/home/hacker$ /challenge/run
    Congratulations, you have become Zardus! Here is your flag:
    pwn.college{ElMBvmBthhQ36wyMhY2jfk88uAJ.dZTN0UDL1cTN0czW}

## Cracking Passwords

I cracked the password using john command and later switched user to zardus and ran /challenge/run.

    hacker@users-cracking-passwords:~$ john /challenge/shadow-leak
    Loaded 1 password hash (crypt, generic crypt(3) [?/64])
    Press 'q' or Ctrl-C to abort, almost any other key for status
    0g 0:00:00:16 0% 2/3 0g/s 279.2p/s 279.2c/s 279.2C/s keller..nation
    aardvark (zardus)
    1g 0:00:00:20 100% 2/3 0.04798g/s 279.4p/s 279.4c/s 279.4C/s Johnson..buzz
    Use the "--show" option to display all of the cracked passwords reliably
    Session completed
    hacker@users-cracking-passwords:~$ su zardus
    Password: aardvark
    zardus@users-cracking-passwords:/home/hacker$ /challenge/run
    Congratulations, you have become Zardus! Here is your flag:
    pwn.college{0QHpK8gjzKxxsrxVfj7iSBQJKMZ.ddTN0UDL1cTN0czW}

## Using sudo

I used sudo command to access and read the flag.

    hacker@users-using-sudo:~$ sudo cat /flag
    pwn.college{QucEQzwX6P3hXzEVN8toh2jHLFK.dhTN0UDL1cTN0czW}

