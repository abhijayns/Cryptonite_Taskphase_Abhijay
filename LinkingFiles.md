#**Comprehending Commands**

##**Linking Files**

- A **hard** link is when you address your appartment using multiple addresses that all lead directly to the same place (e.g., Apt 2 vs Unit 2).
- A **soft** link is when you move appartments and have the postal service automatically forward your mail from your old place to your new place.
- A **symbolic** link (symlink) is created with the _ln_ command with the _\-s_ argument

_hacker@commands~linking-files:/$ cd /_

_hacker@commands~linking-files:/$ ln -s /flag /home/hacker/not-the-flag_

_hacker@commands~linking-files:/$ /challenge/catflag_

_About to read out the /home/hacker/not-the-flag file!_
