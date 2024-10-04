#**Practicing Piping**

##**Redirecting Errors**

I ran _/challenge/run_ ,redirected the output to the file _myflag_ and “errors”

to _instructions_. Later read the _instructions_ and _myflag_ for the flag.

_hacker@piping-redirecting-errors:~$ /challenge/run > myflag 2> instructions_

_hacker@piping-redirecting-errors:~$ cat instructions_

_\[INFO\] WELCOME! This challenge makes the following asks of you:_

_\[INFO\] - the challenge will check that output is redirected to a specific file path : myflag_

_\[INFO\] - the challenge will check that error output is redirected to a specific file path : instructions_

_\[INFO\] - the challenge will output a reward file if all the tests pass : /flag_

_\[HYPE\] ONWARDS TO GREATNESS!_

_\[INFO\] This challenge will perform a bunch of checks._

_\[INFO\] If you pass these checks, you will receive the /flag file._

_\[TEST\] You should have redirected my stdout to a file called myflag. Checking..._

_\[PASS\] The file at the other end of my stdout looks okay!_

_\[TEST\] You should have redirected my stderr to instructions. Checking..._

_\[PASS\] The file at the other end of my stderr looks okay!_

_\[PASS\] Success! You have satisfied all execution requirements._

_hacker@piping-redirecting-errors:~$ cat myflag_

_\[FLAG\] Here is your flag:_

_\[FLAG\] pwn.college{gOOErUxHvRQr6CeDbxGWnIUddm8.ddjN1QDL1cTN0czW}_
