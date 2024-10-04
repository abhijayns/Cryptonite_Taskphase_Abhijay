#**Practicing Piping**

##**Grepping Live Output**

I grepped the flag from _/challenge/run_ using the _|_ (piped operator).

_hacker@piping-grepping-live-output:~$ /challenge/run | grep pwn.college_

_\[INFO\] WELCOME! This challenge makes the following asks of you:_

_\[INFO\] - the challenge checks for a specific process at the other end of stdout : grep_

_\[INFO\] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt_

_\[HYPE\] ONWARDS TO GREATNESS!_

_\[INFO\] This challenge will perform a bunch of checks._

_\[INFO\] If you pass these checks, you will receive the /challenge/.data.txt file._

_\[TEST\] You should have redirected my stdout to another process. Checking..._

_\[TEST\] Performing checks on that process!_

_\[INFO\] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep._

_\[INFO\] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8)._

_\[INFO\] To pass the checks, the executable must be grep._

_\[PASS\] You have passed the checks on the process on the other end of my stdout!_

_\[PASS\] Success! You have satisfied all execution requirements._

_pwn.college{8x8g7Iu-F7ubGjn8muq-mmMSV7c.dlTM4QDL1cTN0czW}_
