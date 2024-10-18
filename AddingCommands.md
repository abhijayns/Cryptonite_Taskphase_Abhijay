#**Pondering Path**

##**Adding Commands**

I passed /bin/cat /flag to the shell script named win and set PATH variable using export command. I also learnt the absolute path of the cat command.

    _hacker@path-adding-commands:~$ nano win_

    _hacker@path-adding-commands:~$ chmod +x /home/hacker/win_

    _hacker@path-adding-commands:~$ export PATH=/home/hacker:$PATH_

    _hacker@path-adding-commands:~$ /challenge/run_

    _Invoking 'win'...._

    _pwn.college{oTTwViDVNRimelhE8hJN7EeqXNv.dZzNyUDL1cTN0czW}_
