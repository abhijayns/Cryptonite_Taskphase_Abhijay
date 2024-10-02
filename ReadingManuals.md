#**Digesting Documentation**

##**Reading manuals**

I displayed the manual page for _challenge_ using man command and passed _\--uentea 895_ argument to _/challenge/challenge_ to get the flag

_hacker@man~reading-manuals:/opt/radare2/libr/flag$ cd /_

_hacker@man~reading-manuals:/$ man challenge_

_CHALLENGE(1) Challenge Commands CHALLENGE(1)_

_NAME_

_/challenge/challenge - print the flag!_

_SYNOPSIS_

_challenge OPTION_

_DESCRIPTION_

_Output the flag when called with the right arguments._

_\--fortune_

_read a fortune_

_\--version_

_output version information and exit_

_\--uentea NUM_

_print the flag if NUM is 895_

_AUTHOR_

_Written by Zardus._

_REPORTING BUGS_

_The repository for this dojo: &lt;<https://github.com/pwncollege/linux-luminarium/>&gt;_

_SEE ALSO_

_man(1) bash-builtins(7)_

_hacker@man~reading-manuals:/$ /challenge/challenge --uentea 895_

_Correct usage! Your flag: pwn.college{Quente8arNjzRw9s50C_iB7W_mw.dRTM4QDL1cTN0czW}_
