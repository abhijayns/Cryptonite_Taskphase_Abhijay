#**Pondering Paths**

##**The Root**

I invoked a program by providing its path on command line.  

    _/pwn_


##**Program and absolute paths**

I executed the _run_ file that is in the _challenge_ directory that is, in turn, in the _/_ directory.  

    _/challenge/run_

##**Position thy self**

Changed the directory using _cd_ command and later ran the challenge program 

    _cd /_
    _/challenge/run_


##**Position elsewhere**

Changed the directory using _cd_ command and later ran the challenge program  

    _cd /_
    _/challenge/run_


##**Position yet elsewhere**

Changed the directory using _cd_ command and later ran the challenge program  

    _hacker@paths~position-yet-elsewhere:/$ cd /usr/bin_

    _hacker@paths~position-yet-elsewhere:/usr/bin$ /challenge/run_

    _Correct!!!_

    _/challenge/run is an absolute path, invoked from the right directory!_


##**Implicit relative paths, from**

Changed the directory using _cd_ command and later ran the challenge program as relative path.   

    hacker@paths-implicit-relative-paths-from-:/$ cd /
    hacker@paths-implicit-relative-paths-from-:/$ challenge/run_

    _Correct!!!_

    _challenge/run is a relative path, invoked from the right directory!_


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

    _hacker@paths-home-sweet-home:~/Desktop$ /challenge/run ~/h_

    _Writing the file to /home/hacker/h!_

    _... and reading it back to you:_

    _pwn.college{U_Idt15ElIAiqqyRQOxcRBJBPcO.dNzM4QDL1cTN0czW}_
























