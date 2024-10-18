#**Pondering Path**

##**Adding Commands**

I passed /bin/cat /flag to the shell script named win and set PATH variable using export command. I also learnt the absolute path of the cat command.

    hacker@path-adding-commands:~$ nano win

    hacker@path-adding-commands:~$ chmod +x /home/hacker/win

    hacker@path-adding-commands:~$ export PATH=/home/hacker:$PATH

    hacker@path-adding-commands:~$ /challenge/run

    Invoking 'win'....

    pwn.college{oTTwViDVNRimelhE8hJN7EeqXNv.dZzNyUDL1cTN0czW}
