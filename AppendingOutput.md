#**Practicing Piping**

##**Appending Output**

I ran _/challenge/run_ with an append-mode redirect of the output to the file _/home/hacker/the-flag_.

_hacker@piping-appending-output:~$ /challenge/run >> /home/hacker/the-flag_

_\[INFO\] WELCOME! This challenge makes the following asks of you:_

_\[INFO\] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag_

_\[HYPE\] ONWARDS TO GREATNESS!_

_\[INFO\] This challenge will perform a bunch of checks._

_\[INFO\] Good luck!_

_\[TEST\] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking..._

_\[HINT\] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor._

_\[HINT\] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are_

_\[HINT\] creating and trying to pass in FDs in python._

_\[PASS\] The file at the other end of my stdout looks okay!_

_\[PASS\] Success! You have satisfied all execution requirements._

_I will write the flag in two parts to the file /home/hacker/the-flag! I'll do_

_the first write directly to the file, and the second write, I'll do to stdout_

_(if it's pointing at the file). If you redirect the output in append mode, the_

_second write will append to (rather than overwrite) the first write, and you'll_

_get the whole flag!_

_hacker@piping-appending-output:~$ cat the-flag_

_|_

_\\|/ This is the first half:_

_v_

_pwn.college{8xerKzZCk9AeoKwhDV6A18sy1xc.ddDM5QDL1cTN0czW}_

_^_

_that is the second half /|\\_

_|_
