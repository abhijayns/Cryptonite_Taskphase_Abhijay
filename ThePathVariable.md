#**Pondering Path**

##**The Path Variable**

I set _PATH=""_ implying the shell to only search in the current directory for executable programs. And later ran _/challenge/run_ to get the flag.


    hacker@path-the-path-variable:~$ PATH=""
    hacker@path-the-path-variable:~$ /challenge/run
    Trying to remove /flag...
    /challenge/run: line 4: rm: No such file or directory
    The flag is still there! I might as well give it to you!
    pwn.college{QDzz0-Ef0HMBgoEAtNBAEYh_cot.dZzNwUDL1cTN0czW}

