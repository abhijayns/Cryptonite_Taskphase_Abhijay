#**Pondering Paths**

##**The Root**

I invoked a program by providing its path on command line.  

    /pwn


##**Program and absolute paths**

I executed the _run_ file that is in the _challenge_ directory that is, in turn, in the _/_ directory.  

    /challenge/run

##**Position thy self**

Changed the directory using _cd_ command and later ran the challenge program 

    cd /
    /challenge/run


##**Position elsewhere**

Changed the directory using _cd_ command and later ran the challenge program  

    cd /
    /challenge/run


##**Position yet elsewhere**

Changed the directory using _cd_ command and later ran the challenge program  

    hacker@paths~position-yet-elsewhere:/$ cd /usr/bin

    hacker@paths~position-yet-elsewhere:/usr/bin$ /challenge/run

    Correct!!!

    /challenge/run is an absolute path, invoked from the right directory!


##**Implicit relative paths, from**

Changed the directory using _cd_ command and later ran the challenge program as relative path.   

    hacker@paths-implicit-relative-paths-from-:/$ cd /
    hacker@paths-implicit-relative-paths-from-:/$ challenge/run

    Correct!!!

    challenge/run is a relative path, invoked from the right directory!


##**Explicit relative paths, from**

Changed the directory using _cd_ command and later ran the _challenge_ program as explicit relative path.  

    hacker@paths-explicit-relative-paths-from-:~$ cd /
    hacker@paths-explicit-relative-paths-from-:/$ ./challenge/run
    Correct!!!
    ./challenge/run is a relative path, invoked from the right directory!

##**Implicit relative path**

Changed the directory using _cd_ command and later ran the _challenge_ program.  

    hacker@paths-implicit-relative-path-:~$ cd /
    hacker@paths-implicit-relative-path-:/$ ./run

    Correct!!!

##**Home sweet home**

Ran the _challenge_ program with an argument.  

    hacker@paths-home-sweet-home:~/Desktop$ /challenge/run ~/h

    Writing the file to /home/hacker/h!

    ... and reading it back to you:

    pwn.college{U_Idt15ElIAiqqyRQOxcRBJBPcO.dNzM4QDL1cTN0czW}
























