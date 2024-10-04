#**Practicing Piping**

##**Grepping Stored Results**

I redirected _/challenge/run_ to _/tmp/data.txt_ and grepped the flag from _/tmp/data.txt_ .

_hacker@piping-grepping-stored-results:~$ /challenge/run > /tmp/data.txt_

_\[INFO\] WELCOME! This challenge makes the following asks of you:_

_\[INFO\] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt_

_\[INFO\] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt_

_\[HYPE\] ONWARDS TO GREATNESS!_

_\[INFO\] This challenge will perform a bunch of checks._

_\[INFO\] If you pass these checks, you will receive the /challenge/.data.txt file._

_\[TEST\] You should have redirected my stdout to a file called /tmp/data.txt. Checking..._

_\[HINT\] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor._

_\[HINT\] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are_

_\[HINT\] creating and trying to pass in FDs in python._

_\[PASS\] The file at the other end of my stdout looks okay!_

_\[PASS\] Success! You have satisfied all execution requirements._

_hacker@piping-grepping-stored-results:~$ grep pwn.college /tmp/data.txt_

_pwn.college{grJT77lE2jg_q3tRkv6jLGR3J8O.dhTM4QDL1cTN0czW}_
