#**Chaining Commands**

##**Redirecting Script Output**

I created a shell script using the _touch_ command, then I used _nano_ command to enter the shell and wrote the two commands which were supposed to be written and then used the _bash_ command, piped its output to _/challenge/solve_ and got the flag.

_hacker@chaining-redirecting-script-output:~$ touch x.sh_

_hacker@chaining-redirecting-script-output:~$ nano x.sh_

_hacker@chaining-redirecting-script-output:~$ bash x.sh | /challenge/solve_

_Correct! Here is your flag:_

_pwn.college{sn9LqJbhIedqdLp--DWDJggFrkf.dhTM5QDL1cTN0czW}_
