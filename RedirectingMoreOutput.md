#**Practicing Piping**

##**Redirecting More Output**

I redirected _/challenge/run_ command’s output to the file _myflag_ and read _myflag_.

_hacker@piping~redirecting-more-output:~$ /challenge/run > myflag_

_\[INFO\] WELCOME! This challenge makes the following asks of you:_

_\[INFO\] - the challenge will check that output is redirected to a specific file path : myflag_

_\[INFO\] - the challenge will output a reward file if all the tests pass : /flag_

_\[HYPE\] ONWARDS TO GREATNESS!_

_\[INFO\] This challenge will perform a bunch of checks._

_\[INFO\] If you pass these checks, you will receive the /flag file._

_\[TEST\] You should have redirected my stdout to a file called myflag. Checking..._

_\[PASS\] The file at the other end of my stdout looks okay!_

_\[PASS\] Success! You have satisfied all execution requirements._

_hacker@piping~redirecting-more-output:~$ cat myflag_

_\[FLAG\] Here is your flag:_

_\[FLAG\] pwn.college{EqGaJTNzIVS6xxVpZAD6ulZaChW.dVjN1QDL1cTN0czW}_
