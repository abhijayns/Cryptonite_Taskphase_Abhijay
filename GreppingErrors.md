#**Practicing Piping**

##**Grepping errors**

I grepped the flag from _errors_ using the _|_ (piped operator) and _\>&_ operator.

The shell has _\>&_ operator, which redirects a file descriptor _to another file descriptor_. 
This means that we can have a two-step process to grep through errors:
First, we redirect standard error to standard output (_2>& 1_) and then pipe the now combined _stderr_ and _stdout_ as normal (_|_).

_hacker@piping-grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college_

_\[INFO\] WELCOME! This challenge makes the following asks of you:_

_\[INFO\] - the challenge checks for a specific process at the other end of stderr : grep_

_\[INFO\] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt_

_\[HYPE\] ONWARDS TO GREATNESS!_

_\[INFO\] This challenge will perform a bunch of checks._

_\[INFO\] If you pass these checks, you will receive the /challenge/.data.txt file._

_\[TEST\] You should have redirected my stderr to another process. Checking..._

_\[TEST\] Performing checks on that process!_

_\[INFO\] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep._

_\[INFO\] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8)._

_\[INFO\] To pass the checks, the executable must be grep._

_\[PASS\] You have passed the checks on the process on the other end of my stderr!_

_\[PASS\] Success! You have satisfied all execution requirements._

_pwn.college{EKtaOC2zlxr32pVSH_dpbuhkUTF.dVDM5QDL1cTN0czW}_
