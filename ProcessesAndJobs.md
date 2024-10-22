# Processes and Jobs

## Listing Processes

I listed running processes using the _ps_ command and ran the renamed file containing the flag.

    hacker@processes-listing-processes:~$ ps -ef
    UID PID PPID C STIME TTY TIME CMD
    root 1 0 0 13:33 ? 00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /ru
    root 7 1 0 13:33 ? 00:00:00 /run/dojo/bin/sleep 6h
    root 68 1 0 13:33 ? 00:00:00 /challenge/13771-run-12707
    root 72 68 0 13:33 ? 00:00:00 sleep 6h
    hacker 73 0 0 13:33 pts/0 00:00:00 /run/dojo/bin/ssh-entrypoint
    hacker 90 73 0 13:33 pts/0 00:00:00 ps -ef
    hacker@processes-listing-processes:~$ ps aux
    USER PID %CPU %MEM VSZ RSS TTY STAT START TIME COMMAN_
    root 1 0.1 0.0 1056 640 ? Ss 13:33 0:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bi
    root 7 0.0 0.0 5052 2240 ? S 13:33 0:00 /run/dojo/bin/sleep 6h
    root 68 0.0 0.0 4132 2560 ? S 13:33 0:00 /challenge/13771-run-12707
    root 72 0.0 0.0 2744 1280 ? S 13:33 0:00 sleep 6h
    hacker 73 0.1 0.0 5372 3840 pts/0 Ss 13:33 0:00 /run/dojo/bin/ssh-entrypoint
    hacker 91 0.0 0.0 7868 3520 pts/0 R+ 13:33 0:00 ps aux
    hacker@processes-listing-processes:~$ /challenge/13771-run-12707
    Yahaha, you found me! Here is your flag:
    pwn.college{ELyM1XAQ7GBBBQ4ws84MUkpnKvq.dhzM4QDL1cTN0czW}
    Now I will sleep for a while (so that you could find me with 'ps').

## Killing Processes

I found the dont_run process and killed it using kill command and later ran /challenge/run to get the flag.

    hacker@processes-killing-processes:~$ ps -ef | grep dont_run
    hacker 73 71 0 17:16 ? 00:00:00 /challenge/dont_run
    hacker 112 75 0 17:17 pts/1 00:00:00 grep --color=auto dont_run
    hacker@processes-killing-processes:~$ kill 73
    hacker@processes-killing-processes:~$ /challenge/run
    Great job! Here is your payment:
    pwn.college{0B4fRJS4NtX6FzGhxB16khq4Vlp.dJDN4QDL1cTN0czW}

## Interrupting Processes

I ran /challenge/run and interrupted it using the hotkey Ctrl-C.

    hacker@processes-interrupting-processes:~$ /challenge/run
    I could give you the flag... but I won't, until this process exits. Remember,
    you can force me to exit with Ctrl-C. Try it now!
    ^C
    Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
    pwn.college{o1ggva_4Few6IwkJEL1R5ldbwrq.dNDN4QDL1cTN0czW}

## Suspending Processes

I ran /challenge/run, suspended it and later ran /challenge/run.

    hacker@processes-suspending-processes:~$ /challenge/run
    I'll only give you the flag if there's already another copy of me running in
    this terminal... Let's check!
    UID PID PPID C STIME TTY TIME CMD
    root 99 66 0 12:04 pts/0 00:00:00 bash /challenge/run
    root 101 99 0 12:04 pts/0 00:00:00 ps -f
    I don't see a second me!
    To pass this level, you need to suspend me and launch me again! You can
    background me with Ctrl-Z or, if you're not ready to do that for whatever
    reason, just hit Enter and I'll exit!
    ^Z
    [1]+ Stopped /challenge/run
    hacker@processes-suspending-processes:~$ /challenge/run
    I'll only give you the flag if there's already another copy of me running in
    this terminal... Let's check!
    UID PID PPID C STIME TTY TIME CMD
    root 99 66 0 12:04 pts/0 00:00:00 bash /challenge/run
    root 106 66 0 12:05 pts/0 00:00:00 bash /challenge/run
    root 108 106 0 12:05 pts/0 00:00:00 ps -f
    Yay, I found another version of me! Here is the flag:
    pwn.college{MKV1W-G_pquTgb9TZzJ232oesMd.dVDN4QDL1cTN0czW}

## Resuming Processes

I ran /challenge/run, suspended it, resumed it using fg command and ran /challenge/run.

    hacker@processes-resuming-processes:~$ /challenge/run
    Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me withthe 'fg' command! Or just press Enter to quit me!
    ^Z
    [1]+ Stopped /challenge/run
    hacker@processes-resuming-processes:~$ fg /challenge/run
    I'm back! Here's your flag:
    pwn.college{sKVugEMWg6R4vZCpMLKPNtFv36E.dZDN4QDL1cTN0czW}

## Backgrounding Processes

I ran /challenge/run, suspended it, backgrounded it using bg command and ran /challenge/run.


    hacker@processes-backgrounding-processes:~$ /challenge/run
    I'll only give you the flag if there's already another copy of me running *and
    not suspended* in this terminal... Let's check!
    UID PID STAT CMD
    root 99 S+ bash /challenge/run
    root 101 R+ ps -o user=UID,pid,stat,cmd
    I don't see a second me!
    To pass this level, you need to suspend me, resume the suspended process in the
    background, and then launch a new version of me! You can background me with
    Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
    do that for whatever reason, just hit Enter and I'll exit!
    ^Z
    [1]+ Stopped /challenge/run
    hacker@processes-backgrounding-processes:~$ bg
    [1]+ /challenge/run &
    hacker@processes-backgrounding-processes:~$
    Yay, I'm now running the background! Because of that, this text will probably
    overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
    to scroll this text out.
    /challenge/run
    I'll only give you the flag if there's already another copy of me running *and
    not suspended* in this terminal... Let's check!
    UID PID STAT CMD
    root 99 S bash /challenge/run
    root 109 S sleep 6h
    root 110 S+ bash /challenge/run
    root 112 R+ ps -o user=UID,pid,stat,cmd
    Yay, I found another version of me running in the background! Here is the flag:
    pwn.college{MZVWG0zEaaSoLKflVm-VTXjk5CM.ddDN4QDL1cTN0czW}

## Foregrounding Processes

    I ran /challenge/run, suspended it, backgrounded it, foregrounded it using fg command and ran /challenge/run.
    hacker@processes-foregrounding-processes:~$ /challenge/run
    To pass this level, you need to suspend me, resume the suspended process in the
    background, and *then* foreground it without re-suspending it! You can
    background me with Ctrl-Z (and resume me in the background with 'bg') or, if
    you're not ready to do that for whatever reason, just hit Enter and I'll exit!
    ^Z
    [1]+ Stopped /challenge/run
    hacker@processes-foregrounding-processes:~$ bg
    [1]+ /challenge/run &
    Yay, I'm now running the background! Because of that, this text will probably
    overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
    to scroll this text out. After that, resume me into the foreground with 'fg';
    I'll wait.
    hacker@processes-foregrounding-processes:~$ fg
    /challenge/run
    YES! Great job! I'm now running in the foreground. Hit Enter for your flag!
    pwn.college{0KcQtb_5_GyE9BcjNuQ-ebh0oz9.dhDN4QDL1cTN0czW}

## Starting Backgrounded Processes

I ran /challenge/run backgrounded by appending it with &.

    hacker@processes-starting-backgrounded-processes:~$ /challenge/run &
    [1] 99
    Yay, you started me in the background! Because of that, this text will probably
    overlap weirdly with the shell prompt, but you're used to that by now...
    Anyways! Here is your flag!
    pwn.college{0HKbW3J69YVgPQBeI315VpmgQdi.dlDN4QDL1cTN0czW}
    [1]+ Done /challenge/run

## Process Exit Codes

I retrieved the exit code returned by _/challenge/get-code_ and ran _/challenge/submit-code_ with that error code as an argument.

    hacker@processes-process-exit-codes:~$ /challenge/get-code
    Exiting with an error code!
    hacker@processes-process-exit-codes:~$ echo $?
    40
    hacker@processes-process-exit-codes:~$ /challenge/submit-code 40
    CORRECT! Here is your flag:
    pwn.college{AzKzWkD38boXfBnOs8a5gVvjSd6.dljN4UDL1cTN0czW}
