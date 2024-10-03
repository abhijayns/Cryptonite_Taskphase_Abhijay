#**File Globbing**

##**Matching with _?_**

When it encounters a _?_ character in any argument, the shell will treat it as **single-character** wildcard. This works like _\*_, but only matches _one_ character. I changed the directory to _/challenge_ using _?_ globbing.

_hacker@globbing-matching-with-:~$ cd /?ha??enge_

_hacker@globbing-matching-with-:/challenge$ /challenge/run_

_You ran me with the working directory of /challenge! Here is your flag:_

_pwn.college{8KVJFj7HsM7XL4YuLjbhb3m2AVO.dJjM4QDL1cTN0czW}_
