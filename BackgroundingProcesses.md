#**Processes and Jobs**

##**Backgrounding Processes**

I ran _/challenge/run_, suspended it, backgrounded it using _bg_ command and ran _/challenge/run_.

_hacker@processes-resuming-processes:~$ /challenge/run_

_Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with_

_the 'fg' command! Or just press Enter to quit me!_

_^Z_

_\[1\]+ Stopped /challenge/run_

_hacker@processes-resuming-processes:~$ fg_

_/challenge/run_

_I'm back! Here's your flag:_

_pwn.college{sKVugEMWg6R4vZCpMLKPNtFv36E.dZDN4QDL1cTN0czW}_

_Don't forget to press Enter to quit me!_

_client_loop: send disconnect: Broken pipe_

_root@ABHIJAY:~# ssh -i ./key hacker@dojo.pwn.college_

_Connected!_

_hacker@processes-backgrounding-processes:~$ /challenge/run_

_I'll only give you the flag if there's already another copy of me running \*and_

_not suspended\* in this terminal... Let's check!_

_UID PID STAT CMD_

_root 99 S+ bash /challenge/run_

_root 101 R+ ps -o user=UID,pid,stat,cmd_

_I don't see a second me!_

_To pass this level, you need to suspend me, resume the suspended process in the_

_background, and then launch a new version of me! You can background me with_

_Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to_

_do that for whatever reason, just hit Enter and I'll exit!_

_^Z_

_\[1\]+ Stopped /challenge/run_

_hacker@processes~backgrounding-processes:~$ bg_

_\[1\]+ /challenge/run &_

_hacker@processes~backgrounding-processes:~$_

_Yay, I'm now running the background! Because of that, this text will probably_

_overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times_

_to scroll this text out._

_/challenge/run_

_I'll only give you the flag if there's already another copy of me running \*and_

_not suspended\* in this terminal... Let's check!_

_UID PID STAT CMD_

_root 99 S bash /challenge/run_

_root 109 S sleep 6h_

_root 110 S+ bash /challenge/run_

_root 112 R+ ps -o user=UID,pid,stat,cmd_

_Yay, I found another version of me running in the background! Here is the flag:_

_pwn.college{MZVWG0zEaaSoLKflVm-VTXjk5CM.ddDN4QDL1cTN0czW}_
