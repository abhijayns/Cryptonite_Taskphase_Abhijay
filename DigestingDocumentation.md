# Digesting Documentation

## Learning from documentation

As mentioned in the description of the challenge, the need for documentation is to figure out how to use all the dang programs, and a specific case of that is figuring out what arguments to specify on the command line.

I learnt to invoke _/challenge/challenge_ command by passing it the argument of _\--giveflag ._

    hacker@man~learning-from-documentation:/opt/radare2/libr/flag$ cd /
    hacker@man~learning-from-documentation:/$ /challenge/challenge --giveflag
    Correct argument!
## Learning Complex Usuage

I learnt to print arbitrary files to the terminal, using the --printfile argument.

The argument to the --printfile argument is the path of the flag to read.

    hacker@man~learning-complex-usage:/opt/radare2/libr/flag$ cd /
    hacker@man~learning-complex-usage:/$ /challenge/challenge --printfile /flag
    Correct argument! Here is the /flag file:
    pwn.college{kSER6T8eprNvK-WxfjnWcNVdGVK.dVjM5QDL1cTN0czW}

## Reading manuals

I displayed the manual page for challenge using man command and passed --uentea 895 argument to /challenge/challenge to get the flag

    hacker@man~reading-manuals:/opt/radare2/libr/flag$ cd /

    hacker@man~reading-manuals:/$ man challenge

    CHALLENGE(1) Challenge Commands CHALLENGE(1)

    NAME

    /challenge/challenge - print the flag!

    SYNOPSIS
    challenge OPTION

    DESCRIPTION

    Output the flag when called with the right arguments.

    --fortune

    read a fortune

    --version

    output version information and exit

    --uentea NUM

    print the flag if NUM is 895

    AUTHOR

    Written by Zardus.
      
    REPORTING BUGS

    The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

    SEE ALSO

    man(1) bash-builtins(7)

    hacker@man~reading-manuals:/$ /challenge/challenge --uentea 895

    Correct usage! Your flag: pwn.college{Quente8arNjzRw9s50C_iB7W_mw.dRTM4QDL1cTN0czW}

## Searching manuals

I learnt to search the manual using / and ? to get --vfnx argument which prints the flag when /challenge/challenge is passed to --vfnx argument.

    hacker@man~searching-manuals:/opt/radare2/libr/flag$ cd /

    hacker@man~searching-manuals:/$ man challenge

    hacker@man~searching-manuals:/$ /challenge/challenge --vfnx

    Initializing...

    Correct usage! Your flag: pwn.college{kVsy6oA_XgrggK1swSp1Zmzhg5v.dVTM4QDL1cTN0czW}

## Searching for manuals

I learnt to search the manual of manual using man man command and found the manual of challenge using man -k /challenge/challenge command and inturn found the manual of

    /challenge/challenge- print the flag! and printed the flag.

    hacker@man~searching-for-manuals:/opt/radare2/libr/flag$ cd /

    hacker@man~searching-for-manuals:/$ man -k challenge

    sdgyalijfp (1) - print the flag!

    hacker@man~searching-for-manuals:/$ man sdgyalijfp

    hacker@man~searching-for-manuals:/$ /challenge/challenge --sdgyal 434

    Correct usage! Your flag: pwn.college{sdg4yFaliYjfU_FpFKcSa3WaKLX.dZTM4QDL1cTN0czW}

## Helpful programs

I read a program's documentation with --help command.

    hacker@man~helpful-programs:/$ cd /

    hacker@man~helpful-programs:/$ /challenge/challenge –help

    hacker@man~helpful-programs:/$ /challenge/challenge --print-value

    The secret value is: 431

    hacker@man~helpful-programs:/$ /challenge/challenge -g 431

    Correct usage! Your flag: pwn.college{sJx4xi3ib1n-IuAPwpktc400kHS.ddjM4QDL1cTN0czW}

## Help for builtins

I passed challenge to help builtin to get the correct argument that displays the flag.

    hacker@man~help-for-builtins:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ cd /

    hacker@man~help-for-builtins:/$ help challenge

    hacker@man~help-for-builtins:/$ challenge --secret gmJM8GPR

    Correct! Here is your flag!

    pwn.college{gmJM8GPRbQ-hDpKoGn58A5MEkg2.dRTM5QDL1cTN0czW}

