# File Globbing

## Matching with 

I changed the directory to _/challenge_ with less than four characters using globbing.

    hacker@globbing-matching-with-:~$ cd /ch\*
    hacker@globbing-matching-with-:/challenge$ /challenge/run
    You ran me with the working directory of /challenge! Here is your flag:
    pwn.college{UC9JBdxpwx5MI9crv8l7MM5IN4M.dFjM4QDL1cTN0czW}

## Matching with ?

When it encounters a ? character in any argument, the shell will treat it as single-character wildcard. This works like *, but only matches one character. I changed the directory to /challenge using ? globbing.

    hacker@globbing-matching-with-:~$ cd /?ha??enge
    hacker@globbing-matching-with-:/challenge$ /challenge/run
    You ran me with the working directory of /challenge! Here is your flag:
    pwn.college{8KVJFj7HsM7XL4YuLjbhb3m2AVO.dJjM4QDL1cTN0czW}

## Matching with []

I changed the working directory to /challenge/files and ran /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h .

    hacker@globbing~matching-with-:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ cd /challenge/files
    hacker@globbing~matching-with-:/challenge/files$ /challenge/run file[bash]
    You got it! Here is your flag!
    pwn.college{UPdneUnpXRTDackwEcDaUhTXl0T.dNjM4QDL1cTN0czW}

## Mathcing Paths with []

I ran /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files.

    hacker@globbing-matching-paths-with-:-$ cd /home/hacker hacker@globbing-matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash] 
    You got it! Here is your flag!       
    pwn.college{8XNmf7gbo8S008EmO015K5Cs7OU.dRjM4QDL1cTN0czW}

## Mixing Globs

I changed the working directory to to /challenge/files and ran /challenge/run with a single, short (6 characters or less) glob that matched the files "_challengin_g", "educational", and "pwning".

    hacker@globbing-mixing-globs:~$ cd /challenge/files
    hacker@globbing-mixing-globs:/challenge/files$ /challenge/run [cep]*
    You got it! Here is your flag!
    pwn.college{kAYK2_C_r_iFT4Rx2j0yU4Wf-4W.dVjM4QDL1cTN0czW

## Exclusionary Globbing

I changed the working directory to to /challenge/files and ran /challenge/run with all files that don't start with p, w, or n.

    hacker@globbing-exclusionary-globbing:~$ cd /challenge/files
    hacker@globbing-exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
    You got it! Here is your flag!
    pwn.college{sHcz4LaQGXSVDxyQGfMZJUZx5Kf.dZjM4QDL1cTN0czW}
