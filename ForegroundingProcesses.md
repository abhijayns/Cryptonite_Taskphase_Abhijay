#**Processes and Jobs**

##**Foregrounding Processes**

I ran _/challenge/run_, suspended it, backgrounded it, foregrounded it using _fg_ command and ran _/challenge/run_.

_hacker@processes-foregrounding-processes:~$ /challenge/run_

_To pass this level, you need to suspend me, resume the suspended process in the_

_background, and \*then\* foreground it without re-suspending it! You can_

_background me with Ctrl-Z (and resume me in the background with 'bg') or, if_

_you're not ready to do that for whatever reason, just hit Enter and I'll exit!_

_^Z_

_\[1\]+ Stopped /challenge/run_

_hacker@processes-foregrounding-processes:~$ bg_

_\[1\]+ /challenge/run &_

_Yay, I'm now running the background! Because of that, this text will probably_

_overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times_

_to scroll this text out. After that, resume me into the foreground with 'fg';_

_I'll wait._

_hacker@processes-foregrounding-processes:~$ fg_

_/challenge/run_

_YES! Great job! I'm now running in the foreground. Hit Enter for your flag!_

_pwn.college{0KcQtb_5_GyE9BcjNuQ-ebh0oz9.dhDN4QDL1cTN0czW}_
