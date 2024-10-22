# Practicing Piping

## Redirecting Output

I used the input redirection to write the word _PWN_ (all uppercase) to the filename _COLLEGE_ (all uppercase).

    hacker@piping-redirecting-output:~$ echo PWN > COLLEGE
    Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
    flag:
    pwn.college{AyXhM0GVUFTOtd5Xtbc8Kyk7A41.dRjN1QDL1cTN0czW}

## Redirecting More Output

I redirected /challenge/run command’s output to the file myflag and read myflag.

    hacker@piping-redirecting-more-output:~$ /challenge/run > myflag

    [INFO] WELCOME! This challenge makes the following asks of you:

    [INFO] - the challenge will check that output is redirected to a specific file path : myflag
  
    [INFO] - the challenge will output a reward file if all the tests pass : /flag

    [HYPE] ONWARDS TO GREATNESS!

    [INFO] This challenge will perform a bunch of checks.

    [INFO] If you pass these checks, you will receive the /flag file.

    [TEST] You should have redirected my stdout to a file called myflag. Checking...

    [PASS] The file at the other end of my stdout looks okay!

    [PASS] Success! You have satisfied all execution requirements.
  
    hacker@piping-redirecting-more-output:~$ cat myflag

    [FLAG] Here is your flag:

    [FLAG] pwn.college{EqGaJTNzIVS6xxVpZAD6ulZaChW.dVjN1QDL1cTN0czW}

## Appending Output

I ran /challenge/run with an append-mode redirect of the output to the file /home/hacker/the-flag.

    hacker@piping-appending-output:~$ /challenge/run >> /home/hacker/the-flag
    [INFO] WELCOME! This challenge makes the following asks of you:
    [INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag
    [HYPE] ONWARDS TO GREATNESS!
    [INFO] This challenge will perform a bunch of checks.
    [INFO] Good luck!
    [TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...
    [HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
    [HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
    [HINT] creating and trying to pass in FDs in python.
    [PASS] The file at the other end of my stdout looks okay!
    [PASS] Success! You have satisfied all execution requirements.
    I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
    the first write directly to the file, and the second write, I'll do to stdout
    (if it's pointing at the file). If you redirect the output in append mode, the
    second write will append to (rather than overwrite) the first write, and you'll
    get the whole flag!
    hacker@piping-appending-output:~$ cat the-flag

     |
     | This is the first half:
     v
    pwn.college{8xerKzZCk9AeoKwhDV6A18sy1xc.ddDM5QDL1cTN0czW}

                                    ^
      that is the second half       |
                                    |

## Redirecting Errors

I ran /challenge/run ,redirected the output to the file myflag and “errors” to instructions. Later read the instructions and myflag for the flag.

    hacker@piping-redirecting-errors:~$ /challenge/run > myflag 2> instructions
    hacker@piping-redirecting-errors:~$ cat instructions
    [INFO] WELCOME! This challenge makes the following asks of you:
    [INFO] - the challenge will check that output is redirected to a specific file path : myflag
    [INFO] - the challenge will check that error output is redirected to a specific file path : instructions
    [INFO] - the challenge will output a reward file if all the tests pass : /flag
    [HYPE] ONWARDS TO GREATNESS!
    [INFO] This challenge will perform a bunch of checks.
    [INFO] If you pass these checks, you will receive the /flag file.
    [TEST] You should have redirected my stdout to a file called myflag. Checking...
    [PASS] The file at the other end of my stdout looks okay!
    [TEST] You should have redirected my stderr to instructions. Checking...
    [PASS] The file at the other end of my stderr looks okay!
    [PASS] Success! You have satisfied all execution requirements.
    hacker@piping-redirecting-errors:~$ cat myflag
    [FLAG] Here is your flag:
    [FLAG] pwn.college{gOOErUxHvRQr6CeDbxGWnIUddm8.ddjN1QDL1cTN0czW}              

## Redirecting Input

I redirected COLLEGE to PWN and then redirected PWN to /challenge/run.

    hacker@piping-redirecting-input:~$ echo COLLEGE > PWN
    hacker@piping-redirecting-input:~$ /challenge/run < PWN
    Reading from standard input...
    Correct! You have redirected the PWN file into my standard input, and I read
    the value 'COLLEGE' out of it!
    Here is your flag:
    pwn.college{k-9P_EWcpZ49E1aN-GIZFnwOCRJ.dBzN1QDL1cTN0czW}

## Grepping Stored Results

I redirected /challenge/run to /tmp/data.txt and grepped the flag from /tmp/data.txt .

    hacker@piping-grepping-stored-results:~$ /challenge/run > /tmp/data.txt

    [INFO] WELCOME! This challenge makes the following asks of you:

    [INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt

    [INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

    [HYPE] ONWARDS TO GREATNESS!

    [INFO] This challenge will perform a bunch of checks.

    [INFO] If you pass these checks, you will receive the /challenge/.data.txt file.
  
    [TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

    [HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.

    [HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are

    [HINT] creating and trying to pass in FDs in python.

    [PASS] The file at the other end of my stdout looks okay!

    [PASS] Success! You have satisfied all execution requirements.

    hacker@piping-grepping-stored-results:~$ grep pwn.college /tmp/data.txt

    pwn.college{grJT77lE2jg_q3tRkv6jLGR3J8O.dhTM4QDL1cTN0czW}

## Grepping Live Output

I grepped the flag from /challenge/run using the | (piped operator).

    hacker@piping-grepping-live-output:~$ /challenge/run | grep pwn.college

    [INFO] WELCOME! This challenge makes the following asks of you:

    [INFO] - the challenge checks for a specific process at the other end of stdout : grep

    [INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

    [HYPE] ONWARDS TO GREATNESS!

    [INFO] This challenge will perform a bunch of checks.
  
    [INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

    [TEST] You should have redirected my stdout to another process. Checking...

    [TEST] Performing checks on that process!

    [INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.

    [INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).

    [INFO] To pass the checks, the executable must be grep.

    [PASS] You have passed the checks on the process on the other end of my stdout!

    [PASS] Success! You have satisfied all execution requirements.

    pwn.college{8x8g7Iu-F7ubGjn8muq-mmMSV7c.dlTM4QDL1cTN0czW}

## Grepping errors

I grepped the flag from errors using the | (piped operator) and >& operator.

The shell has >& operator, which redirects a file descriptor to another file descriptor. This means that we can have a two-step process to grep through errors: First, we redirect standard error to standard output (2>& 1) and then pipe the now combined stderr and stdout as normal (|).

    hacker@piping-grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
    [INFO] WELCOME! This challenge makes the following asks of you:
    [INFO] - the challenge checks for a specific process at the other end of stderr : grep
    [INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt
    [HYPE] ONWARDS TO GREATNESS!
    [INFO] This challenge will perform a bunch of checks.
    [INFO] If you pass these checks, you will receive the /challenge/.data.txt file.
    [TEST] You should have redirected my stderr to another process. Checking...
    [TEST] Performing checks on that process!
    [INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
    [INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
    [INFO] To pass the checks, the executable must be grep.
    [PASS] You have passed the checks on the process on the other end of my stderr!
    [PASS] Success! You have satisfied all execution requirements.
    pwn.college{EKtaOC2zlxr32pVSH_dpbuhkUTF.dVDM5QDL1cTN0czW}

## Duplicating Piped Data with tee

I piped /challenge/pwn into /challenge/college and intercepted the data using tee to see the missing argument.

    hacker@piping-duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn_output | /challenge/college

    Processing...

    The input to 'college' does not contain the correct secret code! This code

    should be provided by the 'pwn' command. HINT: use 'tee' to intercept the

    output of 'pwn' and figure out what the code needs to be.

    hacker@piping-duplicating-piped-data-with-tee:~$ cat pwn_output

    Usage: /challenge/pwn --secret [SECRET_ARG]

    hacker@piping-duplicating-piped-data-with-tee:~$ /challenge/pwn --secret MfN

    856YP | tee pwn1_output | /challenge/college

    Processing...

    Correct! Passing secret value to /challenge/college...

    Great job! Here is your flag:

    pwn.college{MfN856YPEz6EpX0vOcqblNvgf2M.dFjM5QDL1cTN0czW}

## Writing to multiple programs

I ran the /challenge/hack command, and duplicated its output as input to both the /challenge/the and the /challenge/planet commands.

    hacker@piping-writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)

    This secret data must directly and simultaneously make it to /challenge/the and /challenge/planet. Don't try to copy-paste it; it changes too fast.

    17012285451005324256

    Congratulations, you have duplicated data into the input of two programs! Here

    is your flag:

    pwn.college{8QlwudJQlICuhqc38155zYSRWFA.dBDO0UDL1cTN0czW}

## Split-piping sterr and stdout

I piped stderr of /challenge/hack into /challenge/the and stdout of /challenge/hack into /challenge/planet.

    hacker@piping-split-piping-stderr-and-stdout:~$ /challenge/hack 2> >( /challenge/the ) > >( /challenge/planet )
    Congratulations, you have learned a redirection technique that even experts
    struggle with! Here is your flag:
    pwn.college{4hoF16nZnhW3A6v9oCcz5R5M5_4.dFDNwYDL1cTN0czW}

