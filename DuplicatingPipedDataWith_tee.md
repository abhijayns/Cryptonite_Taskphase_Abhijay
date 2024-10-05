#**Practicing Piping**

##**Duplicating Piped Data with tee**

I piped _/challenge/pwn_ into _/challenge/college_ and intercepted the data using _tee_ to see the missing argument.

_hacker@piping-duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn_output | /challenge/college_

_Processing..._

_The input to 'college' does not contain the correct secret code! This code_

_should be provided by the 'pwn' command. HINT: use 'tee' to intercept the_

_output of 'pwn' and figure out what the code needs to be._

_hacker@piping-duplicating-piped-data-with-tee:~$ cat pwn_output_

_Usage: /challenge/pwn --secret \[SECRET_ARG\]_

_hacker@piping-duplicating-piped-data-with-tee:~$ /challenge/pwn --secret MfN_

_856YP | tee pwn1_output | /challenge/college_

_Processing..._

_Correct! Passing secret value to /challenge/college..._

_Great job! Here is your flag:_

_pwn.college{MfN856YPEz6EpX0vOcqblNvgf2M.dFjM5QDL1cTN0czW}_
