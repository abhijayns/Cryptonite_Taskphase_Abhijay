#**Chaining Commands**

##**Executable Shell Scripts**

I created a shell script using the _touch_ command, then I used _nano_ command to enter the shell and wrote _/challenge/solve_. Later I ran the shell script using the command _./shell.sh_


    hacker@chaining-executable-shell-scripts:~$ touch shell.sh
    hacker@chaining-executable-shell-scripts:~$ nano shell.sh
    hacker@chaining-executable-shell-scripts:~$ ./shell.sh
    ssh-entrypoint: ./shell.sh: Permission denied
    hacker@chaining-executable-shell-scripts:~$ ~/shell.sh
    ssh-entrypoint: /home/hacker/shell.sh: Permission denied
    hacker@chaining-executable-shell-scripts:~$ ls -l /shell.sh
    ls: cannot access '/shell.sh': No such file or directory
    hacker@chaining-executable-shell-scripts:~$ chmod 700 shell.sh
    hacker@chaining-executable-shell-scripts:~$ ./shell.sh
    Congratulations on your shell script execution! Your flag:
    pwn.college{YqDLyl-qIZf51z3_hLQlh4h9fhF.dRzNyUDL1cTN0czW}
