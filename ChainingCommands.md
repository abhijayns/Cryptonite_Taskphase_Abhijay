# Chaining Commands

## Chaining with semicolons

I used _;_ to chain _/challenge/pwn_ and _/challenge/college_ and ran them.

    hacker@chaining-chaining-with-semicolons:~$ /challenge/pwn; /challenge/college
    Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
    pwn.college{Exq0lnVqpLmpgQ1qxemi0KDW1CE.dVTN4QDL1cTN0czW}

## Your First Shell Script

I had to research on how to write inside of a shell as nothing was working and I couldn’t solve the question. The source which I referred is https://cloudxlab.com/assessment/displayslide/63/writing-first-shell-script. Reading the website, I learnt that the nano command had to be used to write inside of a shell and exit the shell with the key combination Ctrl+X and save the text. So firstly, I created a shell script using the touch command, then I used nano command to enter into the shell and wrote the two commands which were supposed to be written and then used the bash command and got the flag.

    hacker@chaining-your-first-shell-script:~$ bash
    _Please name your script with an '.sh' extension. This isn't strictly necessary
    eventually, but we'll keep things explicit for the next few levels.
    hacker@chaining-your-first-shell-script:~$ touch x.sh
    hacker@chaining-your-first-shell-script:~$ nano x.sh

I wrote /challenge/pwn; /challenge/college inside the shell

    hacker@chaining-your-first-shell-script:~$ bash x.sh
    Great job, you've written your first shell script! Here is the flag:
    pwn.college{0OJTOmvMXDXxYwbs2JLTMXMc21P.dFzN4QDL1cTN0czW}

## Redirecting Script Output

I created a shell script using the touch command, then I used nano command to enter the shell and wrote the two commands which were supposed to be written and then used the bash command, piped its output to /challenge/solve and got the flag.

    hacker@chaining-redirecting-script-output:~$ touch x.sh
    hacker@chaining-redirecting-script-output:~$ nano x.sh
    hacker@chaining-redirecting-script-output:~$ bash x.sh | /challenge/solve
    Correct! Here is your flag:
    pwn.college{sn9LqJbhIedqdLp--DWDJggFrkf.dhTM5QDL1cTN0czW}

## Executable Shell Scripts

I created a shell script using the touch command, then I used nano command to enter the shell and wrote /challenge/solve inside it. Later I ran the shell script using the command ./shell.sh

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

